# Candidates to verify

Leads for 3D, cell-resolution datasets with per-cell instance segmentation that are **not yet confirmed** (labels not located, nuclei/neurite-only, derived data, or only seen in a catalogue). When verified, move the entry to [README.md](README.md); if rejected, move it to the rejected list below with the reason.

Last updated: 2026-10-06.

## Mouse tooth development: dataset leads (issue #1)

Scope: issue #1 asks for 2D or 3D mouse tooth-development datasets that are segmented or ready to segment. This is broader than the cell-level focus of the rest of this repository, so these leads are kept apart from the main tables. Searched on 2026-10-06 in Zenodo, DataCite (covers Dryad, Figshare, FaceBase), BioStudies/BioImage Archive, IDR, MorphoSource and Europe PMC.

**Result: no public dataset of developing mouse teeth with segmentation labels was found.** The records below are the closest matches that were opened and read.

### Images you could segment

| Record | Stage / tissue | Data | Labels | License | Size | Verdict |
|---|---|---|---|---|---|---|
| [Raw X-ray projections and reconstructed micro-CT stacks, 7-week-old WT and Per2 KO mouse hemimandibles](https://zenodo.org/records/19871122) (Zenodo, 2026; also listed as 10.5281/zenodo.19871121) | 7-week-old mouse hemimandibles with incisor and molar (supports a study of amelogenesis) | 3D micro-CT: raw projections and reconstructed stacks for 4 WT and 4 Per2 KO samples, with acquisition parameters | None | CC-BY-4.0 | 8 zip archives, about 14.6 GB in total | Best "to segment" match. Adult mice, so it is not a developmental series |
| [Raw data for Piper and Green, cap-to-bell molar morphogenesis, J Anat 2025](https://kcl.figshare.com/articles/dataset/Raw_data_associated_with_the_article_Piper_C_and_Green_J_B_A_b_Cap-to-bell_stage_molar_tooth_morphogenesis_occurs_through_proliferation-independent_sulcus_sharpening_and_condensation-associated_tension_in_the_dental_papilla_b_Journal_of_Ana/27733866/1) (King's College London, DOI 10.18742/27733866.v1) | Developing mouse molar, cap-to-bell stage, explants and DAPI-stained slices | 2D raw TIFFs, morphometric files, R code | Includes a StarDist model for DAPI nuclei and the resulting nuclear point clouds; no instance masks described | CC-BY-SA-4.0 | 763 MB | Only developmental-stage record found, but 2D and nuclei-level |
| [MorphoSource, mouse molar micro-CT meshes](https://www.morphosource.org/catalog/media?locale=en&search_field=all_fields&q=mouse+molar+development) (e.g. *Mus musculus domesticus* first upper molars, data manager R. Ledevin) | Adult wild-caught specimens | Micro-CT with surface meshes, "Open Download" | None found | In Copyright (per catalogue) | 425 hits for the query; only the top results were read | Morphometrics material, not developmental; check individual records and rights before use |

### Checked and not suitable

| Record | Why not |
|---|---|
| [Multi-modal characterization of rodent dental development](https://doi.org/10.5061/dryad.9p8cz8wvn) (Dryad, CC0, 2025) | Postnatal mouse incisor and first molar (micro-CT, nanoindentation, EDS, Raman), but the deposit is only 8.8 MB, so it most likely holds measurements rather than image volumes (file list not opened). Related paper: 10.1021/acsami.5c08408 |
| [Mapping molar shapes on signaling pathways](https://zenodo.org/records/4278031) (Zenodo, CC0, 2020) | Two CSV files of molar shape data derived from 3D surface models; no images |
| BioStudies / BioImage Archive search | Only transcriptomics (e.g. E-MTAB-12557, E-MTAB-12544 tooth organoids) and literature records; no tooth imaging study |
| IDR title search ("tooth", "dental") | No studies |

### Paper only

| Paper | Notes |
|---|---|
| [Micro-CT analysis of tooth development of C57BL/6 mice strain](https://europepmc.org/article/MED/36854424) (Tang et al., Chin J Stomatol 2023, DOI 10.3760/cma.j.cn112144-20220802-00433) | Micro-CT of 54 C57BL/6 mice at nine stages from P1 to P56 (n=6 per stage), the closest match to a developmental series. Not open access, in Chinese, and the abstract mentions no data deposit. Contact the authors to ask whether the scans can be shared. A paper is not a dataset |

### Not yet opened

- Dryad datasets on mouse molar phenotypes: [10.5061/dryad.70585](https://doi.org/10.5061/dryad.70585) (BMP7 deletion) and [10.5061/dryad.bm770](https://doi.org/10.5061/dryad.bm770) (third molar size). They may contain micro-CT or surface data.
- FaceBase project [10.25550/9n-6d8m](https://doi.org/10.25550/9n-6d8m), amelogenin phosphorylation: the record describes developing enamel analyses, but whether image data are attached is unknown. FaceBase hosts other craniofacial micro-CT deposits worth browsing.
- Synchrotron (ESRF) mouse molar volume, [10.13140/rg.2.2.14729.03686](https://doi.org/10.13140/rg.2.2.14729.03686), a 2010 unpublished record.
- MorphoSource: filter by age or stage metadata to find juvenile specimens.

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
