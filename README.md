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
| Cell Tracking Challenge: 3D+time simulated sets (Fluo-C3DH-A549-SIM, Fluo-N3DH-SIM+) | Simulated A549 cells; simulated HL60 nuclei | Simulated fluorescence | Whole cell / nuclei | Exact computer-generated masks for all cells (absolute truth) | 314 MB and 3.1 GB training sets | Not stated on pages read | [CTC 3D datasets](https://celltrackingchallenge.net/3d-datasets/), [annotations](https://celltrackingchallenge.net/annotations/) | - | **Synthetic.** The real 3D+time sets (e.g. Fluo-N3DH-CE, Fluo-N3DL-DRO) have only partial gold segmentation truth and silver truth for some; they are not listed here. Masks are tracked over time. |

## B. 3D datasets without segmentation (raw only)

| Dataset | Organism / tissue | Modality | Size | License | Link | Year | Notes |
|---|---|---|---|---|---|---|---|
| Three-Dimensional Mechanical Cooperativity Optimises Epithelial Wound Healing (S-BSST3135) | *D. melanogaster*, wing disc (wound healing) | Not stated on page | One 11.07 GB zip of source data (EMBOJ-2025-123351.zip) | CC0 | [BioStudies](https://www.ebi.ac.uk/biostudies/studies/S-BSST3135) (DOI 10.6019/S-BSST3135) | 2026 | Lim, Vicente-Munuera, Tetley, Mao. Supplied by maintainer as not segmented. |
| EMPIAR Volume EM Gallery (28 volumes) | Various: HeLa, human organoid, *A. thaliana* root, *Platynereis*, zebrafish, placenta... | FIB-SEM, SBF-SEM, array tomography | 28 volumes, viewable and downloadable as OME-Zarr | Not read | [Volume EM gallery](https://beta.bioimagearchive.org/bioimage-archive/galleries/volumeem) | - | Raw volume EM across species; individual studies may have segmentations elsewhere. Not checked per volume. |

## Candidates to verify

Unverified and borderline leads are in [CANDIDATES.md](CANDIDATES.md). Entries move into the tables above only once checked against the inclusion criteria.

## Sources searched

| Source | URL | Status | Last checked |
|---|---|---|---|
| BioImage Archive, AI-ready studies gallery (13 studies) | https://beta.bioimagearchive.org/bioimage-archive/galleries/ai/ai-ready-studies | Fully reviewed | 2026-10-06 |
| BioImage Archive, Volume EM gallery | https://beta.bioimagearchive.org/bioimage-archive/galleries/volumeem | Listing reviewed | 2026-10-06 |
| BioStudies S-BSST3135 | https://www.ebi.ac.uk/biostudies/studies/S-BSST3135 | Reviewed | 2026-10-06 |
| bioimage.io datasets | https://bioimage.io/#/datasets | Reviewed (46 datasets in the public collection index) | 2026-10-06 |
| Zenodo | https://zenodo.org | Two keyword searches reviewed; more needed | 2026-10-06 |
| IDR | https://idr.openmicroscopy.org | Title searches ("segmentation", "3D", "instance") reviewed; more needed | 2026-10-06 |
| Cell Tracking Challenge | https://celltrackingchallenge.net | 3D+time datasets and annotation policy reviewed | 2026-10-06 |
| OSF (Arabidopsis atlas) | https://osf.io/fzr56/ | Reviewed | 2026-10-06 |
| Figshare, Dryad, OpenOrganelle, EMPIAR (segmentation entries), Allen Cell, Mendeley Data, BBBC | - | Pending | - |

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
| 2026-10-06 | README structure created. Added 9 verified datasets/collections (Section A), 2 raw-only entries (Section B). Candidates tracked in CANDIDATES.md. |

## Author

Pablo Vicente Munuera, UCL Mao Lab / TissueMechanicsLab

## License

See [LICENSE](LICENSE).
