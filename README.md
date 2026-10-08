# 3D_images_datasets_to_segment_or_already_segmented

A collection of public 3D datasets at **cellular resolution** in which **individual cells are instance-segmented** (one unique label per cell), with information about organism, study and other metadata. Datasets that are not segmented are listed separately when they are still useful.

Only entries whose record page was opened and checked are listed here. Unverified leads live in [CANDIDATES.md](CANDIDATES.md).

Inspired by [Histopathology-Datasets](https://github.com/Pablo1990/Histopathology-Datasets).

## Overview

- [Inclusion criteria](#inclusion-criteria)
- [A. 3D datasets with cell instance segmentation](#a-3d-datasets-with-cell-instance-segmentation)
- [B. 3D datasets without segmentation (raw only)](#b-3d-datasets-without-segmentation-raw-only)
- [Candidates to verify](#candidates-to-verify)
- [Sources searched](#sources-searched)
- [Table field definitions](#table-field-definitions)
- [Contributing](#contributing)
- [Update log](#update-log)

## Inclusion criteria

1. **3D**: volumetric images (z-stacks, light-sheet, EM/FIB-SEM, micro-CT, etc.).
2. **Cellular resolution**: individual cells can be resolved.
3. **Instance segmentation** (Section A): each cell has its own label. Semantic-only masks, bounding boxes and point annotations are not enough. Nuclei-instance labels are allowed but marked `nuclei` in *Label target*.
4. **Openly accessible** with a stable identifier (DOI, accession or persistent URL).
5. License stated where available. "Not stated" means the record page we read does not give one; check before reuse.

## A. 3D datasets with cell instance segmentation

| Dataset | Organism / tissue | Modality | Label target | Label origin | Size | License | Link | Year | Notes |
|---|---|---|---|---|---|---|---|---|---|
| 3D cell shape of *Drosophila* wing disc (S-BIAD843) | *D. melanogaster*, wing disc | Confocal, multi-photon | Whole cell | Software-assisted + expert manual | 8 volumes, 36-105 z-slices, 512x512, ~60 MiB, OME-Zarr | CC0 | [BioImage Archive](https://www.ebi.ac.uk/bioimage-archive/galleries/S-BIAD843-ai.html) | 2023 | Paci, Fernandez Mosquera, Vicente Munuera, Mao. |
| PlantSeg core datasets: Ovules of *Arabidopsis thaliana* (S-BIAD1392) | *A. thaliana*, ovules (fixed) | Confocal | Whole cell (cell boundaries) | Watershed in MorphoGraphX + expert hand correction | 31 volume/mask pairs (62 files), 4.48 GB | CC0 | [BioImage Archive](https://beta.bioimagearchive.org/bioimage-archive/galleries/ai/ai-ready-study/S-BIAD1392) | 2024 | Tofanelli, Vijayan, Schneitz, Wolny, Kreshuk, Zulueta-Coarasa. PlantSeg paper: [Wolny et al., eLife 2020](https://doi.org/10.7554/eLife.57613). Also on bioimage.io (`piquant-burger`, listed there as CC-BY-4.0). |
| PlantSeg core datasets: Lateral root primordia of *Arabidopsis thaliana* (S-BIAD1367) | *A. thaliana*, lateral root primordia | SPIM (light-sheet) | Whole cell (cell boundaries) | ilastik multicut bootstrapping, iterative refinement with Paintera proofreading | 56 files, 1.99 GB | CC0 | [BioImage Archive](https://beta.bioimagearchive.org/bioimage-archive/galleries/ai/ai-ready-study/S-BIAD1367) | 2024 | Louveaux, Maizel, Wolny, Kreshuk, Zulueta-Coarasa. Also on bioimage.io (`nourishing-baguette`). |
| CartoCell: 3D epithelial cysts | Epithelial cysts (see paper for species/cell type) | Fluorescence (tag on bioimage.io; see paper) | Whole cell | Not stated on record page; see paper | CartoCell.zip, 185.7 MB | CC-BY-4.0 | [Zenodo 10973241](https://zenodo.org/records/10973241), [paper](https://doi.org/10.1016/j.crmeth.2023.100597) | 2023 | Andres-San Roman, Gordillo-Vazquez, Franco-Barranco et al. Zenodo record is a mirror of Mendeley Data (DOI 10.17632/7gbkxgngpm.2). Also on bioimage.io (`divine-melon`). |
| Arabidopsis 3D Digital Tissue Atlas | *A. thaliana*: anther, filament, valve, leaf, petal, root, sepal, pedicel | Confocal | Whole cell | Segmented in MorphoGraphX; README documents mis-segmented cells | Per-tissue TIFF stacks and segmentations, plus meshes (.mgxm/.obj) and cell networks. Total size not stated | Not stated on OSF page | [OSF fzr56](https://osf.io/fzr56/) (DOI 10.17605/OSF.IO/FZR56) | 2019 | Bassel lab. Segmented TIFF retains per-cell labels. Also on bioimage.io (`juicy-peanut`). |
| Peri-implantation mouse embryos | *M. musculus*, embryos | Confocal (nuclei), light-sheet (membrane) | Nuclei (confocal) and membrane-defined cells (light-sheet) | Not stated on record page | Nuclei: 22 train + 13 val stacks; membrane: 5 train + 1 val stacks; 3.1 GB, HDF5 (`raw`, `label`) | CC-BY-4.0 | [Zenodo 6546550](https://zenodo.org/records/6546550) | 2022 | Bondarenko. Record describes `label` as ground-truth instance segmentation. |
| 3D nuclei instance segmentation, *C. elegans* L1 | *C. elegans*, L1 larvae | Confocal (Leica, 63x) | Nuclei | Original annotations from Long et al. 2009, manually curated by Kainmueller | 28 volumes with masks, avg ~1050x140x140 voxels, 84.4 MB | CC-BY-4.0 | [Zenodo 5942575](https://zenodo.org/records/5942575) | 2022 | Long, Peng, Liu, Kim, Myers, Kainmueller, Weigert. Train/val/test split provided. |
| 2D and 3D instance segmentation of nuclei from volume EM (S-BIAD2822) | *H. sapiens*, *M. musculus* | FIB-SEM, SEM | Nuclei | Model (NucleoNet) predictions + expert proofreading in empanada-napari; 3D from orthogonal 2D inference + voting, proofread | 24 files, 1.95 GB | CC0 | [BioImage Archive](https://beta.bioimagearchive.org/bioimage-archive/galleries/ai/ai-ready-study/S-BIAD2822) | 2026 | Narayan (NCI/NIH). |
| Allen Cell hiPSC single-cell image dataset (Quilt package `aics/hipsc_single_cell_image_dataset`) | Human iPS cells (WTC-11 lines), colonies, one fluorescently tagged structure per line plus membrane and DNA dyes | 3D fluorescence; microscope type not stated on the package page | Whole cell and nuclei | Not stated on the package page; the 3DCellComposer paper says the Allen Cell and Structure Segmenter was trained with a human-in-the-loop approach, see [Viana et al.](https://doi.org/10.1038/s41586-022-05563-7) | Per package page: raw field-of-view images (`fov_path`) 6 TB; field-of-view segmentations (`fov_seg_path`, 4 channels: nuclear seg, cell seg, nuclear contour, cell contour; one unique integer per cell) 24.4 GB; single-cell raw crops 7.2 TB and crop masks 93.3 GB; structure masks 7.3 GB; `metadata.csv` 1.7 GB. The Allen download page cites 31,987 3D cell images | Allen Institute [Terms of Use](https://www.allencell.org/terms-of-use.html): research and other noncommercial use, citation required; not an open licence | [Quilt package](https://open.quiltdata.com/b/allencell/packages/aics/hipsc_single_cell_image_dataset), [Allen download page](https://www.allencell.org/data-downloading.html) | 2023 | Maintainers Jianxu Chen and Kim Metzler (Allen Institute for Cell Science). Paper: Viana et al., Nature 2023. Very large; the full-field `.ome-tif` sets are also offered as `.tar.gz` parts of about 20 GB each. Other Allen packages are in CANDIDATES.md. |
| Cell Tracking Challenge: 3D+time simulated sets (Fluo-C3DH-A549-SIM, Fluo-N3DH-SIM+) | Simulated A549 cells; simulated HL60 nuclei | Simulated fluorescence | Whole cell / nuclei | Exact computer-generated masks for all cells (absolute truth) | 314 MB and 3.1 GB training sets | Not stated on pages read | [CTC 3D datasets](https://celltrackingchallenge.net/3d-datasets/), [annotations](https://celltrackingchallenge.net/annotations/) | - | **Synthetic.** The real 3D+time sets (e.g. Fluo-N3DH-CE, Fluo-N3DL-DRO) have only partial gold segmentation truth and silver truth for some; they are not listed here. Masks are tracked over time. |
| 3D epithelial cell topology in *Drosophila* wing discs (S-BIAD3120) | *D. melanogaster*, 3rd instar wing discs (control and Mbs-RNAi) | Two-photon, membrane marker | Whole cell | Not stated on record page; see paper | 12 files (6 volumes + 6 `_labels.tif` masks), 214 MB | CC0 | [BioStudies](https://www.ebi.ac.uk/biostudies/studies/S-BIAD3120) | 2026 | Paci, Berkemeier, Baum, Page, Mao. Record keywords: instance segmentation, 3D. Paper: PNAS 2026 (title "3D epithelial cell topology tunes signalling range to promote precise patterning"). |
| Mouse intestinal organoid, light-sheet, reference OME-Zarr with nuclei tracking (Zenodo 22078388) | *M. musculus*, intestinal organoid (single movie) | Light-sheet 3D time-lapse; membrane (mem9) and nuclear (H2B) channels; z 2.0 um, xy 0.26 um | Nuclei and whole cell (plus semantic lumen/epithelium) | Not stated on record page; see "Multiscale light-sheet organoid imaging framework" | Seven zips from 242 MB (mini) to 39.8 GB (full), OME-Zarr v0.5 | CC-BY-4.0 | [Zenodo 22078388](https://zenodo.org/records/22078388) | 2026 | Hess, Caton, Kothari, Swedlow. Labels are instance segmentations of nuclei and cells per timepoint, but sparse (only cells in the tracking solution; ~350 late in the movie). Nucleus IDs are not tracked across time (lineage tree supplied). Related lead: Zenodo 6828906 in CANDIDATES.md. |
| SBF-SEM volume of gold-nanoparticle-loaded FaDu tumour spheroid with segmentation (S-BIAD3263) | *H. sapiens*, FaDu head-and-neck carcinoma spheroid | SBF-SEM, 10x10x50 nm voxels, ~102x102x35 um | Whole cell, nuclei (and AuNPs) | Fine-tuned Cellpose-SAM predictions; manual ground truth for cells and nuclei on 20 slices at two resolutions | OME-NGFF zarr archive plus ground-truth TIFFs; the first 25 listed files total ~67 GB (121 file records) | CC0 | [BioStudies](https://www.ebi.ac.uk/biostudies/studies/S-BIAD3263) | 2026 | Bottone, Gerken, Habermann, Mateos, Lucas, Riemann et al. Whole-volume masks are model-predicted; only 20 slices are manual. |
| Early gastrulation in *C. elegans*: raw confocal and segmented 3D cell meshes (Zenodo 19795530) | *C. elegans*, early embryo | Confocal (raw stacks in `/microscopy`) | Whole cell (per-cell 3D surface meshes, VTP) | Not stated on record page; see paper | One 17.2 GB zip (contents list not opened) | CC-BY-4.0 | [Zenodo 19795530](https://zenodo.org/records/19795530) | 2026 | Thiels, Jelier, Vanslambrouck, Xiao et al. Segmentations are meshes in `/segmentations`, not label images; the record also holds per-cell volumes, contact areas and curvatures. Paper: "Integrated quantitative imaging and biomechanical modeling of early gastrulation in C. elegans". |

## B. 3D datasets without segmentation (raw only)

| Dataset | Organism / tissue | Modality | Size | License | Link | Year | Notes |
|---|---|---|---|---|---|---|---|
| Three-Dimensional Mechanical Cooperativity Optimises Epithelial Wound Healing (S-BSST3135) | *D. melanogaster*, wing disc (wound healing) | Not stated on page | One 11.07 GB zip of source data (EMBOJ-2025-123351.zip) | CC0 | [BioStudies](https://www.ebi.ac.uk/biostudies/studies/S-BSST3135) (DOI 10.6019/S-BSST3135) | 2026 | Lim, Vicente-Munuera, Tetley, Mao. Supplied by maintainer as not segmented. |
| LimeSeg test datasets: *Drosophila* egg chamber (`DrosophilaEggChamber.tif`) | *D. melanogaster*, egg chamber | Point-scanning confocal; ch.1 DAPI nuclei, ch.2 membranes (Nrg::GFP, Bsg::GFP) | 91 MB TIFF, voxel sizes in metadata | CC-BY-4.0 | [Zenodo 1472859](https://zenodo.org/records/1472859) | 2018 | Raw, no cell labels: segment each cell yourself. Same record also holds a vesicle confocal stack and an 8 GB HeLa FIB-SEM volume. LimeSeg paper (Machado et al.). |
| Time-lapse confocal of a split tooth germ, early stage (SSBD 4348, project ssbd-repos-000100) | *M. musculus*, embryonic tooth germ (transgenic) | Laser-scanning confocal (Zeiss LSM780), time-lapse, 45 min/frame; XY 0.55 um/px, Z 1.82 um | 49.7 GB (24.1 GB zip) | CC BY | [SSBD](https://ssbd.riken.jp/database/dataset/4348/) | 2015 (released 2019) | Yamamoto, Oshima, Tsuji et al., [Sci Rep 2015](https://doi.org/10.1038/srep18393). Raw, no cell labels. Reporter not stated on the record. |
| Time-lapse confocal of a split tooth germ, late stage (SSBD 4349, same project) | *M. musculus*, embryonic tooth germ (transgenic) | Same as above | 80.7 GB (45.9 GB zip) | CC BY | [SSBD](https://ssbd.riken.jp/database/dataset/4349/) | 2015 (released 2019) | Same paper. Raw, no cell labels. |
| Epithelial tissue deformation in tooth development (SSBD ssbd-repos-000098) | *M. musculus*, tooth epithelium | Time-lapse confocal, plus BDML quantitative cell-trajectory data | 12.4 GB | CC BY 4.0 | [SSBD](https://ssbd.riken.jp/repository/ssbd-repos-000098/) | 2016 (released 2019) | Morita, Tsuji et al., [PLoS ONE 2016](https://doi.org/10.1371/journal.pone.0161336). Raw images plus trajectories, not shape labels. |
| EMPIAR Volume EM Gallery (28 volumes) | Various: HeLa, human organoid, *A. thaliana* root, *Platynereis*, zebrafish, placenta... | FIB-SEM, SBF-SEM, array tomography | 28 volumes, viewable and downloadable as OME-Zarr | Not read | [Volume EM gallery](https://beta.bioimagearchive.org/bioimage-archive/galleries/volumeem) | - | Raw volume EM across species; individual studies may have segmentations elsewhere. Not checked per volume. |

## Candidates to verify

Unverified and borderline leads are in [CANDIDATES.md](CANDIDATES.md). Entries move into the tables above only once checked against the inclusion criteria.

## Sources searched

| Source | URL | Status | Last checked |
|---|---|---|---|
| BioStudies / BioImages collection, newest-first search "3D AND (segmentation OR labels)" (140 hits; 40 newest read) | https://www.ebi.ac.uk/biostudies/api/v1/BioImages/search | Reviewed; 5 records opened | 2026-10-07 |
| Europe PMC, mouse tooth + confocal/light-sheet/3D, last ~3 weeks (119 hits) and tooth preprints (5) | https://europepmc.org | Titles screened; nothing with deposited tooth images | 2026-10-07 |
| BioImage Archive, AI-ready studies gallery (13 studies) | https://beta.bioimagearchive.org/bioimage-archive/galleries/ai/ai-ready-studies | Fully reviewed | 2026-10-06 |
| BioImage Archive, Volume EM gallery | https://beta.bioimagearchive.org/bioimage-archive/galleries/volumeem | Listing reviewed | 2026-10-06 |
| BioStudies S-BSST3135 | https://www.ebi.ac.uk/biostudies/studies/S-BSST3135 | Reviewed | 2026-10-06 |
| bioimage.io datasets | https://bioimage.io/#/datasets | Reviewed (46 datasets in the public collection index) | 2026-10-06 |
| BioStudies / BioImages, newest-first search "3D AND (segmentation OR labels OR masks)" (147 hits; 25 newest read, 4 records opened via API) | https://www.ebi.ac.uk/biostudies/api/v1/BioImages/search | Reviewed; nothing qualifying for Section A | 2026-10-08 |
| Zenodo REST, newest-first: segmentation + 3D/confocal/light-sheet (788 hits, 25 newest), organoid/embryo/model organism, tooth, nuclei ground truth | https://zenodo.org/api/records | Reviewed; 1 record opened (23201343), see CANDIDATES.md | 2026-10-08 |
| Europe PMC, mouse tooth/molar/incisor, first published 2026-09-30 to 2026-10-08 (71 hits, titles screened) | https://europepmc.org | No tooth-development or tooth-imaging paper | 2026-10-08 |
| IDR project list (147 projects; newest ids idr0156 to idr0173 scanned by name) | https://idr.openmicroscopy.org/api/v0/m/projects/ | idr0159 opened (description only); others not opened | 2026-10-08 |
| RIKEN SSBD database front page | https://ssbd.riken.jp/database/ | Front page shows 281 database projects (the log of 2026-10-06 said 280); the new project was not identified | 2026-10-08 |
| Zenodo | https://zenodo.org | REST API, newest-first segmentation / 3D / organoid / tooth queries (2026-10-07); more needed | 2026-10-07 |
| IDR | https://idr.openmicroscopy.org | Title searches ("segmentation", "3D", "instance") reviewed; more needed | 2026-10-06 |
| Cell Tracking Challenge | https://celltrackingchallenge.net | 3D+time datasets and annotation policy reviewed | 2026-10-06 |
| OSF (Arabidopsis atlas) | https://osf.io/fzr56/ | Reviewed | 2026-10-06 |
| DataCite (all publishers), Mendeley Data, OSF, Dryad, FaceBase, eMouseAtlas (tooth image queries) | https://api.datacite.org | Reviewed for mouse tooth imaging; see CANDIDATES.md | 2026-10-06 |
| RIKEN SSBD (tooth keyword leads) | https://ssbd.riken.jp | Three tooth projects reviewed; rest of SSBD not searched | 2026-10-06 |
| Allen Cell Explorer data page and Quilt `allencell` bucket (35 packages) | https://www.allencell.org/data-downloading.html | hiPSC single-cell dataset read in full; nuclear dataset 1 read; remaining packages listed in CANDIDATES.md | 2026-10-07 |
| Figshare, OpenOrganelle, EMPIAR (segmentation entries), BBBC | - | Pending | - |

## Table field definitions

| Field | Meaning |
|---|---|
| Dataset | Official title (and accession if any) |
| Organism / tissue | Species and tissue, organoid, embryo or cell culture |
| Modality | Confocal, light-sheet, two-photon, FIB-SEM, etc. |
| Label target | Whole cell, nuclei, or both |
| Label origin | Manual, semi-automatic, or automatic (model/algorithm named) |
| Size | Number of volumes, voxel dimensions, file format and disk size where available |
| License | e.g. CC0, CC-BY 4.0 |
| Link | Persistent URL or DOI, plus paper if available |
| Year | Release year |
| Notes | Caveats, authors, mirrors |

## Contributing

Open a pull request or issue with a new row, filling in as many fields as possible and a verifiable link. Please confirm that labels are per-cell instances and that the data is 3D.

## Update log

| Date | Change |
|---|---|
| 2026-10-08 | No new qualifying datasets found; nothing added to Section A or B. Three new leads and one unopened-IDR lead recorded in CANDIDATES.md. Sources: Zenodo REST (newest-first), BioStudies BioImages search, Europe PMC (tooth), IDR project list, SSBD front page. No new mouse tooth imaging data. WebFetch was blocked for Zenodo and BioStudies, so the browser was used. Figshare, Dryad, OpenOrganelle, EMPIAR, BBBC, Hugging Face not searched this run. |
| 2026-10-07 | Added 4 verified entries to Section A: S-BIAD3120, Zenodo 22078388, S-BIAD3263, Zenodo 19795530. No new qualifying tooth datasets (Europe PMC / Zenodo checked). Sources: Zenodo REST (newest-first), BioStudies BioImages search, Europe PMC. IDR, SSBD, Figshare, Dryad not re-searched this run. |
| 2026-10-06 | README structure created. Added 9 verified datasets/collections (Section A), 2 raw-only entries (Section B). Candidates tracked in CANDIDATES.md. |

## Author

Pablo Vicente Munuera, UCL Mao Lab / TissueMechanicsLab

## License

See [LICENSE](LICENSE).
