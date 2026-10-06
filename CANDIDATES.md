# Candidates to verify

Leads for 3D, cell-resolution datasets with per-cell instance segmentation that are **not yet confirmed** (labels not located, nuclei/neurite-only, derived data, or only seen in a catalogue). When verified, move the entry to [README.md](README.md); if rejected, move it to the rejected list below with the reason.

Last updated: 2026-10-06.

## Mouse tooth development: dataset discovery leads

These are relevant leads and public repository search pages, **not confirmed dataset records**. The paper below describes mouse tooth-development micro-CT, but I have not verified that its scans or segmentations are publicly downloadable. Repository search pages are included to help locate other studies; a search page alone is not evidence that it contains a suitable dataset. Promote only individual records whose files, developmental stage and access terms have been checked.

| Lead / repository | Link | Relevance and status |
|---|---|---|
| Micro-CT analysis of tooth development of C57BL/6 mice strain | [Europe PMC article record (PMID 36854424)](https://europepmc.org/article/MED/36854424) | Relevant mouse tooth-development imaging study. Exact stages and availability of downloadable scans or labels remain unverified; a paper is not itself a dataset. |
| MorphoSource | [Repository](https://www.morphosource.org/) | Search for mouse dental specimens and micro-CT media. No developmental tooth record or associated segmentation was confirmed. |
| Zenodo | [Search: mouse tooth development](https://zenodo.org/search?q=mouse%20tooth%20development) | Search for imaging datasets and supplementary volumes; no matching record was confirmed. |
| Dryad | [Search: mouse tooth development](https://datadryad.org/search?q=mouse%20tooth%20development) | Search for data accompanying tooth-development studies; no matching record was confirmed. |
| Figshare | [Search: mouse tooth development](https://figshare.com/search?q=mouse%20tooth%20development) | Search for study data and supplementary image stacks; no matching record was confirmed. |
| BioImage Archive | [Archive](https://www.ebi.ac.uk/bioimage-archive/) | Search for deposited microscopy and volumetric images; no matching tooth-development record was confirmed. |
| EMPIAR | [Archive](https://www.ebi.ac.uk/empiar/) | Search for electron-microscopy datasets; likely more useful for cellular ultrastructure than whole-tooth morphology. No matching record was confirmed. |

## Leads

| Candidate | Source / link | What we know | Open question |
|---|---|---|---|
| Ovarian reserve oocyte dataset (SPIM, DDX4, 7 ovaries aged 5-60 weeks) | [Zenodo 19085211](https://zenodo.org/records/19085211) (v1, 13.0 GB raw + checkpoint), [Zenodo 20556572](https://zenodo.org/records/20556572) (v2, 1.6 GB example data); [BiaPy tutorial](https://biapy.readthedocs.io/en/latest/tutorials/instance_seg/ovarian-reserve.html); bioimage.io entry says manual 3D instance masks. Both records CC-BY-4.0 | 3D light-sheet, oocytes only | Zenodo records do not clearly contain the instance masks; the tutorial refers to a separate training dataset. Oocytes are one cell type, not all cells |
| NucMM | bioimage.io `exquisite-salad`, DOI 10.5281/zenodo.14870442 (Unlicense) | Zebrafish brain EM (~170,000 nuclei) and mouse micro-CT (~7,000 nuclei); tags: 3D, instance-segmentation | **Nuclei only.** Zenodo record not opened |
| Platynereis EM training data | [Zenodo 3675220](https://zenodo.org/records/3675220), CC-BY-4.0, 6.8 GB (membrane 3.0 GB, nuclei 3.0 GB, cilia, cuticle) | Training blocks from a whole 6-day *Platynereis* SBF-SEM volume (Vergara et al., Cell 2021) | Described as training data for CNN structure segmentation (membranes, nuclei); not confirmed as per-cell instance labels. Whole-body cell segmentation may be released with the PlatyBrowser (check) |
| Multiscale light-sheet organoid imaging framework | [Zenodo 6828906](https://zenodo.org/records/6828906), CC-BY-4.0, 12 GB (full data ~700 GB on request) | Intestinal organoids, light-sheet; keywords include segmentation, tracking | Not confirmed that segmentation masks are included |
| Datasets from "bootstrapping dense 3D segmentations from sparse 2D annotations" | [Zenodo 21223591](https://zenodo.org/records/21223591), 3.9 GB zarr | Aggregated, reformatted public datasets with `labels`, includes `epi` (plant epithelium, light microscopy) | Mostly EM neuropil/organelles; check `epi` and `liconn` provenance and original licenses |
| 3D Cell Instance Segmentation Dataset (BBBC027-derived) | [Zenodo 11072981](https://zenodo.org/records/11072981), CC-BY 3.0, 4.7 GB | 30 3D sets, only annotated slices kept and split into individual 2D images, COCO format | Derived 2D slices, not volumes; check whether BBBC027 is simulated |
| NesSys nuclear segmentation (idr0062) | [IDR](https://idr.openmicroscopy.org), repo [idr0062-blin-nuclearsegmentation](https://github.com/IDR/idr0062-blin-nuclearsegmentation) | 3D nuclei in dense tissue/embryos, 22 images, released 2019 | Nuclei only; confirm that masks/ROIs are in IDR |
| Predicting cell cycle stage from 3D single-cell nuclear images (idr0167) | IDR, repo [idr0167-li-cellcyclenet](https://github.com/IDR/idr0167-li-cellcyclenet) | 3D single-nucleus images, 683 images in two experiments | Study file could not be read; unknown whether instance masks are included |
| ssTEM of *Drosophila* ventral nerve cord (bioimage.io `gourmet-bacon`) | [Source repo](https://github.com/unidesigner/groundtruth-drosophila-vnc), CC-BY-4.0 | 3D EM neurite/neuron segmentation | Neurites rather than whole cells; bioimage.io description is wrongly copied from the Arabidopsis root entry |
| CREMI and SNEMI3D | bioimage.io `crunchy-cookie` (CREMI); SNEMI3D DOI 10.5281/zenodo.15535109 (CC-BY-4.0) | 3D EM neurite instance segmentation | Neurites rather than whole cells; decide whether to include connectomics data |
| Zenodo leads not yet opened | [4419985](https://zenodo.org/records/4419985), [4899944](https://zenodo.org/records/4899944), [5010430](https://zenodo.org/records/5010430), [6376582](https://zenodo.org/records/6376582) | Surfaced by a Zenodo keyword search (epithelium, *Drosophila* embryo, multiscale reconstruction, inner ear organoid) | Everything |
| Real 3D+time Cell Tracking Challenge sets | [CTC 3D datasets](https://celltrackingchallenge.net/3d-datasets/) | Gold segmentation truth has "very limited cell instance coverage"; silver truth has good coverage but is computer-generated | Decide whether partial or silver labels meet the criteria |

## Rejected / out of scope

| Dataset | Source | Reason |
|---|---|---|
| MitoEM, MitoEM 2.0 (S-BIAD2808) | bioimage.io, BioImage Archive | Mitochondria instances, not cells |
| SynapseNet (S-BIAD2534) | BioImage Archive | Synaptic vesicles, not cells |
| HR-Kidney (idr0147) | IDR | Glomeruli and vasculature at organ scale, not cells |
| Embryonic mice ultrasound volumes (S-BIAD686) | BioImage Archive | Body/brain masks, not cells |
| ReSCU-Nets (S-BIAD1410), PhotoFiTT (S-BIAD1269), HeLa nuclei (S-BIAD1659), DSB 2018 subset (S-BIAD1735), nuclear segmentation set (S-BIAD634), zebrafish infection (S-BIAD1159) | BioImage Archive AI-ready gallery | 2D or 2D+time, or not cell instances |
| Cell Instance Segmentation Dataset, CISD | [Zenodo 5938893](https://zenodo.org/records/5938893) | 2D cytology samples (21 focal planes), CC-BY; instance masks are 2D |
| Ellipsoid segmentation of spheroids | [Zenodo 5089728](https://zenodo.org/records/5089728) | 2.5D spheroid-level segmentation, not per-cell |
| DeepBacs, ZeroCostDL4Mic, Omnipose, Lizard, HPA, SpineDL, DSB 2018, MoNuSeg, LIVECell, Covid-IF | bioimage.io | 2D or no 3D per-cell labels |

## Still to search

Figshare, Dryad, OpenOrganelle, EMPIAR (entries with cell segmentations), Allen Cell, Mendeley Data, BBBC, Hugging Face datasets, further IDR and Zenodo queries (organoid, embryo, spheroid, zebrafish, *Drosophila*, plant), the BioImage Archive full search, and daily updates as requested in the project instructions.
