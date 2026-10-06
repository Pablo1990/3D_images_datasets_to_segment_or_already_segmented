# Candidates to verify

Leads for 3D, cell-resolution datasets with per-cell instance segmentation that are **not yet confirmed** (labels not located, nuclei/neurite-only, derived data, or only seen in a catalogue). When verified, move the entry to [README.md](README.md); if rejected, move it to the rejected list below with the reason.

Last updated: 2026-10-06.

## Raw confocal / light-sheet with labelled cells, to segment yourself (2026-10-06)

Looked for 3D fluorescence volumes where cells carry a membrane or nuclear label but no instance labels are needed. Records below were opened through the BioStudies or Zenodo API and the description read; image files themselves were not downloaded, so dimensions, channels and licences need a check before they move to the README.

**Raw, to segment**

| Record | Organism / tissue | Label and modality | Details | Verdict |
|---|---|---|---|---|
| [S-BIAD1134](https://www.ebi.ac.uk/biostudies/studies/S-BIAD1134) | Human MCF10A breast acinus | Light-sheet; H2B-miRFP703 nuclear marker (plus ERK and CDK2 reporters) | One 3D movie, 145 time points, 188x188x188 voxels at 0.29 um, Zarr. Description says nuclear marker is for segmentation and tracking | Good, small. Nuclei only |
| [S-BIAD815](https://www.ebi.ac.uk/biostudies/studies/S-BIAD815) (OME-NGFF copy of idr0051) | Zebrafish tailbud, neuromesodermal progenitor zone | Light-sheet 4D, used for in toto cell tracking | 5 files | Good. Label channel not read |
| [S-BIAD553](https://www.ebi.ac.uk/biostudies/studies/S-BIAD553) | Chick embryo gastrulation | Light-sheet movies of the embryo surface, membrane-GFP line, plus confocal of SNAI2 and pMLC2 | About 1,500 files | Cellular resolution, but the movies are of the surface and may be 2D projections. Check |

**Possibly already segmented (check for Section A)**

| Record | What it is | Verdict |
|---|---|---|
| [S-BSST475](https://www.ebi.ac.uk/biostudies/studies/S-BSST475) (wild type), [S-BSST497](https://www.ebi.ac.uk/biostudies/studies/S-BSST497) (*ino*, 118 ovules), [S-BSST498](https://www.ebi.ac.uk/biostudies/studies/S-BSST498) (WUSCHEL reporter, 69 ovules; z-stack plus mesh, raw cell boundaries and PlantSeg predictions), [S-BIAD957](https://www.ebi.ac.uk/biostudies/studies/S-BIAD957) (*Cardamine hirsuta*) | 3D digital cell atlases of ovule development, cellular resolution, from confocal | Atlases with per-cell data imply cell labels; confirm the segmentation files exist and are per-cell |
| [S-BIAD2102](https://www.ebi.ac.uk/biostudies/studies/S-BIAD2102) (trout, CC BY 4.0), [S-BIAD2103](https://www.ebi.ac.uk/biostudies/studies/S-BIAD2103) (mouse) | Confocal images and masks of adipocytes in situ, 5-DTAF label | Masks are mentioned; confirm they are per-cell instances. Adult tissue |

**Not tooth-specific.** No confocal or light-sheet tooth-development volume was found in BioImage Archive, Zenodo, IDR or Figshare (see the tooth section above).

## Mouse tooth development: dataset leads (issue #1)

Scope: issue #1 asks for 2D or 3D mouse tooth-development datasets that are segmented or ready to segment. This is broader than the cell-level focus of the rest of this repository, so these leads are kept apart from the main tables. Searched on 2026-10-06 in Zenodo, DataCite (covers Dryad, Figshare, FaceBase), BioStudies/BioImage Archive, IDR, MorphoSource and Europe PMC.

**Result: no public dataset of developing mouse teeth with segmentation labels was found.** There is, however, one open developmental micro-CT series ready to segment (FaceBase, E10 to P32). The records below are the closest matches that were opened and read.

### Published 3D confocal datasets of mouse tooth germs to segment

**None found (2026-10-06).** No public confocal or light-sheet volume of a mouse tooth germ (bud, cap, bell stage; molar or incisor), raw or segmented, turned up. Searched from record pages and API descriptions only, nothing downloaded:

| Source | Queries | Result |
|---|---|---|
| BioImage Archive / BioStudies | tooth, molar, incisor, tooth germ, dental epithelium, dental mesenchyme, odontogenesis, enamel knot, cleared jaw light-sheet, craniofacial light-sheet | No tooth-development study. Only S-BIAD2846 (Bmp2/Bmp7, periodontal injury, adult), not opened |
| Zenodo | tooth/molar/incisor/tooth germ with confocal, light-sheet, z-stack, segmentation, live imaging, explant | Fossil papers and clinical CT only |
| IDR | project and screen names and descriptions | idr0144 is bright-field histology of human jaw bone |
| Figshare | tooth development confocal, molar light-sheet, tooth germ 3D, incisor confocal, dental epithelium live imaging | Nearest is [Marin-Riera et al. 2018](https://doi.org/10.1371/journal.pcbi.1005981) (tooth explants, CC BY 4.0): supplementary PNGs, PDFs and one movie, no volumes |
| Europe PMC full-text screen | 39 open-access mouse tooth papers naming a repository | Deposits are micro-CT (FaceBase), sequencing, or measurements; no confocal stacks |

Closest options (none is a confocal tooth germ):

| Record | Why it is close | Gap |
|---|---|---|
| [FaceBase 1-YBZ6](https://doi.org/10.25550/1-YBZ6) | Mouse E10-P32 molar development, 3D, open | Synchrotron micro-CT at about 8.8 um voxels, not cellular, not confocal |
| [Zenodo 1472859](https://zenodo.org/records/1472859) | Raw confocal, nuclei + membrane channels, epithelium, CC-BY-4.0 | *Drosophila* egg chamber, not a tooth |
| [S-BIAD1134](https://www.ebi.ac.uk/biostudies/studies/S-BIAD1134) | Light-sheet 3D, nuclear marker, small | Human breast acinus |

If you need real tooth-germ confocal data, the usual route is to ask the authors of papers that image tooth germs by confocal or light-sheet but do not deposit the stacks.

### Images you could segment

| Record | Stage / tissue | Data | Labels | License | Size | Verdict |
|---|---|---|---|---|---|---|
| [Timing of mouse molar formation is not influenced by jaw length (FaceBase FB00001182)](https://doi.org/10.25550/1-YBZ6) (Boughner et al., J Dev Biol 2021, [PMC8006249](https://pmc.ncbi.nlm.nih.gov/articles/PMC8006249/); project [10.25550/1-Y732](https://doi.org/10.25550/1-Y732)) | Wild-type C57BL/6J mouse heads and jaws, E10 to P32 (23 stages), up to 3 specimens per stage | Synchrotron micro-CT (Canadian Light Source BMIT), silver contrast stain, 8.75-8.9 um voxels; reconstructed in NRecon and rendered as 3D volumes in Amira | None described | FaceBase open-data terms (no license field on the record) | Not stated on the record; file list not opened | **Best developmental match.** A real developmental series, open and ready to segment. Released 2021-06-07 |
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

### Papers with public data (Europe PMC screen, 2026-10-06)

Method: Europe PMC full-text search for open-access papers with tooth/molar/incisor terms and *mouse* in the title or abstract and a mention of Zenodo, Dryad, Figshare, FaceBase, MorphoSource, OSF, BioImage Archive, EMPIAR or IDR (39 papers). Each full text was scanned for its data-availability statement, repository identifiers and imaging terms; the eight most relevant were read in detail. Papers that deposit data somewhere else, or never name a repository, are not captured.

| Paper | Data it deposits | Verdict |
|---|---|---|
| Boughner et al. 2021, J Dev Biol ([PMC8006249](https://pmc.ncbi.nlm.nih.gov/articles/PMC8006249/)) | Micro-CT scans on FaceBase, DOI 10.25550/1-Y732 | Usable; see the table above |
| Paine, Bapat et al. 2026, Front Physiol, *Ambn-IRESCre* ([PMC13272140](https://pmc.ncbi.nlm.nih.gov/articles/PMC13272140/)) | FaceBase [FB00001404](https://doi.org/10.25550/7X-HZDA) and [FB00001355](https://doi.org/10.25550/2W-YN1C): micro-CT of 8-week-old incisor enamel | Adult enamel, not development; record text is minimal and the file list was not opened. Related FaceBase micro-CT records from the same lab: [6P-VWAT](https://doi.org/10.25550/6p-vwat), [2X-XKY8](https://doi.org/10.25550/2x-xky8), [2W-YMZR](https://doi.org/10.25550/2w-ymzr), [2W-YCZ2](https://doi.org/10.25550/2w-ycz2), [2W-RS08](https://doi.org/10.25550/2w-rs08) |
| Hu, Simmer et al., *Slc13a5* and *Odaph* knock-out mice (papers [PMC13513652](https://pmc.ncbi.nlm.nih.gov/articles/PMC13513652/), [PMC13331816](https://pmc.ncbi.nlm.nih.gov/articles/PMC13331816/)) | FaceBase [2N-7V1T](https://doi.org/10.25550/2n-7v1t), [2P-43WM](https://doi.org/10.25550/2p-43wm), [2N-EGT0](https://doi.org/10.25550/2n-egt0): tooth development in knock-out mice | Developing teeth, but the record descriptions only describe how the mice were made. Which images are attached was not checked |
| Hu et al. 2025, Sci Rep, *Dspp* models ([PMC12246090](https://pmc.ncbi.nlm.nih.gov/articles/PMC12246090/)) | FaceBase [5-J8R6](https://doi.org/10.25550/5-J8R6): developing incisors and molars characterised by backscattered SEM, histology and nanohardness | 2D imaging; file list not opened |
| Chai lab, FaceBase [3C-SF82](https://doi.org/10.25550/3c-sf82) and [3B-M1X6](https://doi.org/10.25550/3b-m1x6) | Micro-CT and single-cell RNA-seq of the molar at PN9.5 | Postnatal molar development, but both descriptions are unfinished placeholder text ("In this dataset....") and no paper was linked; may not be public in full |
| He et al. 2026, eLife, whole-tooth regeneration ([PMC13609483](https://pmc.ncbi.nlm.nih.gov/articles/PMC13609483/)); Piezo2 neurons, PNAS 2025 ([PMC12280930](https://pmc.ncbi.nlm.nih.gov/articles/PMC12280930/)); KDM6B, Bone Res 2026 ([PMC13219498](https://pmc.ncbi.nlm.nih.gov/articles/PMC13219498/)); Syndecan-4, Front Physiol 2026 ([PMC13226030](https://pmc.ncbi.nlm.nih.gov/articles/PMC13226030/)); developmental scaling of tooth size, PNAS 2023 ([PMC10288632](https://pmc.ncbi.nlm.nih.gov/articles/PMC10288632/)) | Zenodo or FaceBase records contain sequencing data, or the Zenodo DOI is a cited software release | Rejected: no image data deposited |

Note: FaceBase pages carried the banner "This repository is under review for potential modification in compliance with Administration directives" when read. If you rely on FaceBase deposits, download and mirror them soon.

### Not yet opened

- Dryad datasets on mouse molar phenotypes: [10.5061/dryad.70585](https://doi.org/10.5061/dryad.70585) (BMP7 deletion, [PMC5792877](https://pmc.ncbi.nlm.nih.gov/articles/PMC5792877/)), [10.5061/dryad.bm770](https://doi.org/10.5061/dryad.bm770) (third molar size), [10.5061/dryad.bt848](https://doi.org/10.5061/dryad.bt848) (first upper molar shape, [PMC5679752](https://pmc.ncbi.nlm.nih.gov/articles/PMC5679752/)) and [10.5061/dryad.f4qrfj6sn](https://doi.org/10.5061/dryad.f4qrfj6sn) (aging mice, [PMC7220376](https://pmc.ncbi.nlm.nih.gov/articles/PMC7220376/)). They are named in the papers' data statements but their contents were not opened.
- FaceBase project [10.25550/9n-6d8m](https://doi.org/10.25550/9n-6d8m), amelogenin phosphorylation: the record describes developing enamel analyses, but whether image data are attached is unknown. A FaceBase search for micro-CT returns about 700 records (many are zebrafish); only the tooth-related ones were triaged above.
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
