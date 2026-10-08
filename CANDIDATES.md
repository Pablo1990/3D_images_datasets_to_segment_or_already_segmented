# Candidates to verify

Leads for 3D, cell-resolution datasets with per-cell instance segmentation that are **not yet confirmed** (labels not located, nuclei/neurite-only, derived data, or only seen in a catalogue). When verified, move the entry to [README.md](README.md); if rejected, move it to the rejected list below with the reason.

Last updated: 2026-10-08.

## Daily run 2026-10-08: new leads (record pages / API descriptions read, nothing downloaded)

| Record | What it is | Verdict |
|---|---|---|
| [Zenodo 23201343](https://zenodo.org/records/23201343) (Chu, Chen, Kuo; CC-BY-4.0; 2026-10-07; cFOS.tar 384 MB, Lectin.tar 892 MB, TH.tar 4.07 GB) | Three mouse-brain fluorescence datasets (Lectin vessels, c-Fos neurons, tyrosine hydroxylase neurons) with \"segmentation annotations\", from the FIDELITY study (Lin et al.), for the 3D-GUSL paper (\"A Lightweight Learning Framework for Multi-Biomarker Mouse Brain Lightsheet Microscopy Segmentation\") | Not confirmed. Record does not say whether annotations are per-cell instances or semantic masks, nor voxel size. Tar contents not opened. Neuron markers only (not all cells) |
| [S-BIAD3895](https://www.ebi.ac.uk/biostudies/studies/S-BIAD3895) (DelGiorno, Vanderbilt; CC BY 4.0; 2026-08-08) | Unpublished serial-section 3D EM volume of mouse pancreas with tuft cells and acinar-to-ductal metaplasia, as an arivis Vision4D scene (.vsv) plus six segmentation layers (.vsseg): full segmentation, second tuft cell, ADM nuclei, ADM nuclei plus tuft cell, tuft-cell actin rootlets (single label and individually labelled) | Not confirmed for Section A. Segmentation covers selected cells and structures, not stated as every cell, and is in a proprietary arivis format. File sizes not read |
| [S-BIAD3591](https://www.ebi.ac.uk/biostudies/studies/S-BIAD3591) (CC0; 2026-06-26; MACH3Cancer, French) | Multi-site dual-view oblique plane (light-sheet) imaging of melanoma spheroids with ERK-KTR reporter; each site component includes fused TIFF volumes and \"derived segmentation outputs\"; keywords include nuclear segmentation and single-cell analysis | Not confirmed. Segmentation file type (label images or tables) and size not checked. Nuclei at best. |
| [IDR idr0159](https://idr.openmicroscopy.org) (Tribolium castaneum embryo, \"Non-invasive long-term fluorescence live imaging\") | Fluorescence live imaging of a *Tribolium* embryo; only the project name and a two-line description were read | Possible Section B (raw light-sheet). Image dimensions, licence and cell label channel not checked; no segmentation mentioned |

Not opened (title only, from the BioStudies newest-first list; none looks like a cell-segmentation resource): S-BIAD3383 (Giardia organelle proteins), S-BIAD3989, S-BIAD3794, S-BIAD3379, S-BIAD3928, S-BIAD3429, S-BIAD3803, S-BIAD4000, S-BIAD3885, S-BIAD3802, S-BIAD3228, S-BIAD3788, S-BIAD3750.

Rejected today: S-BIAD3778 (L929 spheroid osmotic response; description is about volume changes, no segmentation stated), S-BIAD2441 (3D human lung development light-sheet, processed data, CC BY-NC 4.0; no cell labels stated; organ-scale, not opened further), Zenodo 23135747 (by title: bright-field fungal filaments; record not opened), Zenodo 23089214 (by title: Reticulon localization in mitosis, 31 MB; record not opened), Europe PMC tooth hits 2026-09-30 to 2026-10-08 (periodontal, orthodontic, clinical; no developmental imaging deposit).

## Daily run 2026-10-07: leads from Zenodo and BioStudies (record pages / API descriptions read, nothing downloaded)

| Record | What it is | Verdict |
|---|---|---|
| [Zenodo 18711581](https://zenodo.org/records/18711581) (Sablowski, Yates; CC-BY-4.0; 2026-02-20; ~44.7 GB) | 3D confocal (Airyscan) stacks of *Arabidopsis* inflorescence apices, processed with Python scripts that segment cells and then manually corrected | Likely Section A. The zips (named "...Airyscan Processing.zip") were not opened, so whether per-cell label images are included is unconfirmed |
| [S-BIAD3984](https://www.ebi.ac.uk/biostudies/studies/S-BIAD3984) (Marques thesis, CC0; 2026-09-30) | Whole-mount larval zebrafish brain, Airyscan confocal; description says 3D Cellpose nuclear masks for ~50,000 neurons per hemisphere | The 21 listed files (~243 GB) all look like image TIFFs; no mask files identified. Nuclei only. Not confirmed |
| [Zenodo 22760592](https://zenodo.org/records/22760592) (Dye, Popovic; CC-BY-4.0; 2026-09-15) | *Drosophila* wing disc ex vivo E-cadherin-GFP spinning-disc z-stack time-lapse, cell boundary segmentation and tracking (TissueMiner database) | Segmentation of the apical junction layer is probably 2D; the description does not say. Not confirmed 3D |
| [Zenodo 17278246](https://zenodo.org/records/17278246) (Schmeisser; CC-BY-4.0; 7.7 GB) | Benchmark compiled from 11 open 3D cell-segmentation datasets for a review | Compilation; check original sources and licences (list is on the project GitLab README, not read) |
| [Zenodo 12859553](https://zenodo.org/records/12859553) (Chen, Murphy; CC-BY-4.0; 11.5 GB) | Segmentation masks from the 3DCellComposer pipeline (tissue 3D images) | Masks are method outputs (record description is one line); tissue type and whether source images are included not stated. Not confirmed |
| [S-BIAD3593](https://www.ebi.ac.uk/biostudies/studies/S-BIAD3593) (CC BY 4.0; 2026-08-09) | Whole mouse ovary light-sheet, AI segmentation of ~85,000 oocytes | Same study as the ovarian reserve lead below; the mask files were not looked at. Oocytes only |
| [Zenodo 21068247](https://zenodo.org/records/21068247) (Giardini, Palandri et al.; CC-BY-4.0) | Whole mouse hearts, dual-mesoSPIM, 6 um isotropic tomograms | Not cellular resolution for the tomograms; other components (4 listed) were not read |
| Zenodo [22639669](https://zenodo.org/records/22639669) (DARE3d-v2) | 3D time-lapse cell-division detection data (10 GB) | Division events, not cell instance labels as far as the description says |
| Europe PMC 42781859, "Cellular basis of accelerated whole-tooth regeneration" (2026-09-24) | New tooth paper | Abstract/deposit not checked; not confirmed mouse developmental imaging |

Resolved: the *Multiscale light-sheet organoid imaging framework* lead (Zenodo 6828906) now has an instance-labelled example movie, Zenodo 22078388 (README Section A). The 6828906 record itself still does not state that masks are included.

Rejected today: Zenodo 23090918 (Microcount glial images; 2D brightfield/widefield), Zenodo 22799027 and 22069319 (by title: warehouse objects, whole rapeseed plants; not cellular), S-BIAD3191 (organoid phenotyping platform; no segmentation masks stated), S-BIAD3547 (Bo-Net bone stromal cell segmentation; title only, record not opened, so 2D/3D unknown).

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

**Found, after an earlier miss (2026-10-06).** My first pass through BioImage Archive, Zenodo, IDR, Figshare and Europe PMC found nothing. A lead list from another source then pointed to RIKEN SSBD, which none of those searches cover, and it holds real time-lapse confocal volumes of mouse tooth germs (table below, now also in the README). All are raw: no cell labels. Record pages only, nothing downloaded.

| Record | Content | Imaging | License | Size | Verdict |
|---|---|---|---|---|---|
| [SSBD dataset 4348](https://ssbd.riken.jp/database/dataset/4348/) (`fig2a_split_toothgerm`, project [ssbd-repos-000100](https://ssbd.riken.jp/repository/ssbd-repos-000100/), Yamamoto et al. 2015, [10.1038/srep18393](https://doi.org/10.1038/srep18393)) | Early stage of a split tooth germ, transgenic mouse embryo, time-lapse | Zeiss LSM780 laser-scanning confocal, fluorescence; XY 0.55 um/px, Z 1.82 um/slice, 45 min per frame | CC BY | 49.7 GB (zip 24.1 GB) | **Best match.** Which fluorescent reporter labels the cells is not on the record; see the paper |
| [SSBD dataset 4349](https://ssbd.riken.jp/database/dataset/4349/) (`fig2b_enamelknot`, same project) | Late stage of the same split tooth germ | Same settings | CC BY | 80.7 GB (zip 45.9 GB) | Same caveat |
| [SSBD ssbd-repos-000098](https://ssbd.riken.jp/repository/ssbd-repos-000098/) (Morita et al. 2016, [10.1371/journal.pone.0161336](https://doi.org/10.1371/journal.pone.0161336)) | Time-lapse confocal of tooth epithelium deformation, with BDML quantitative data (cell trajectories) | Confocal time-lapse | CC BY 4.0 | 12.4 GB | Good; smaller. Trajectories give cell positions, not shapes |

SSBD project 100 also lists micro-CT of the split tooth and of eruption (small zips, 65-80 KB). Lead-list items rejected after checking: Zenodo 8250595 and Dryad qnk98sfkk (same record: RNAscope of *human* fetal tooth germ), Mendeley v3wgx8pm5y (human scRNA-seq and spatial transcriptomics), Zenodo 17185791 (human dentin), 11392406, 10597292 and 8027553 (clinical dental scans), SSBD 105 (dog CT). The GEO and ENA accessions in that list are sequencing records and were not opened.

Earlier searches, kept for the record:

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

Other papers that image tooth germs by confocal but state no deposit are listed in the 2D section below; authors are the route for those.

### 2D images of mouse tooth development, to reconstruct in 3D (2026-10-06)

Looked for 2D sections or fluorescence images of developing mouse teeth that could be aligned and stacked. Record descriptions only; no image files were downloaded, so image counts, section spacing and whether the sections are serial are unconfirmed.

| Record | Stage / tissue | Images | License | Size | Verdict |
|---|---|---|---|---|---|
| [KCL Figshare 10.18742/27733866.v1](https://doi.org/10.18742/27733866.v1) (Piper and Green, J Anat 2025, "Cap-to-bell stage molar tooth morphogenesis...") | Mouse molar explants, cap to bell stage | Raw .tif images behind the figures, including DAPI-stained molar slices; plus a StarDist nucleus-segmentation model, point-cloud nuclear positions, .morphoj measurements and R code | CC BY-SA 4.0 | 763 MB | **Best 2D lead.** Slices are probably single sections per sample, not a serial stack. Check before planning a reconstruction |
| [FaceBase 64-D500](https://doi.org/10.25550/64-d500) | E14.5 *Lhx6*-/- mutant mouse, molar tooth root, 3 embryos | Fluorescence microscopy | Not stated on record | Not stated | Real 2D tooth images, but the description is one line; imaging details and file list not read |

**Checked, not images:** FaceBase [2P-K8WE](https://doi.org/10.25550/2p-k8we) and [2T-8JMG](https://doi.org/10.25550/2t-8jmg) (E14 vestibular lamina and incisor tooth germ, bulk RNA-seq), Zenodo [19343165](https://zenodo.org/records/19343165) (dentinogenesis in human cells and adult mouse molar figures, not development), Figshare [5925484](https://doi.org/10.1371/journal.pcbi.1005981) (Marin-Riera et al. 2018 explant study: supplementary figure PNGs and one movie).

**Papers that image tooth germs but state no data deposit** (author requests are the route): Ahtiainen et al. 2016 ([PMC5021093](https://pmc.ncbi.nlm.nih.gov/articles/PMC5021093/), early tooth budding, live imaging), Panousopoulou and Green 2016 ([PMC4760321](https://pmc.ncbi.nlm.nih.gov/articles/PMC4760321/), molar placode invagination; the data statement found only supplementary files at Development), and the 2016 JCB commentary "Watching a deep dive" ([PMC5021101](https://pmc.ncbi.nlm.nih.gov/articles/PMC5021101/), JCB commentary on live imaging of tooth invagination). First-author names above come from memory and were not checked against the records; supplementary movies were not verified beyond the full-text scan.

**Section atlases (checked 2026-10-06):** [eMouseAtlas (EMAP)](https://www.emouseatlas.org/emap/ema/home.php) offers downloadable 3D reconstructions built from serial histological sections of whole mouse embryos for Theiler stages TS07 to TS26 (`.wlz` files, opened with JAtlasViewer; [downloads index](https://www.emouseatlas.org/emap/ema/theiler_stages/downloads/downloads.html)), and the [eHistology atlas](https://www.emouseatlas.org/emap/eHistology/kaufman/index.php) (Kaufman supplement) has annotated whole-embryo sections. Site content is CC BY 3.0 unless noted. These are whole-embryo images, so tooth germs are a few small structures in each section; whether cells are resolvable was not checked, and which stages show tooth buds, caps and bells was not looked up. GUDMAP and Allen atlases were not searched (kidney and brain focus).

### Sweep of a second lead list and wider repository search (2026-10-06)

Every link in a lead list supplied by the maintainer was checked from record pages or APIs, then DataCite, Dryad, Zenodo and SSBD were swept again for tooth image deposits. Nothing was downloaded. Only the three SSBD records above qualify as mouse tooth-germ confocal data.

| Lead | What it is | Verdict |
|---|---|---|
| SSBD [100](https://ssbd.riken.jp/repository/ssbd-repos-000100/), [98](https://ssbd.riken.jp/repository/ssbd-repos-000098/) | Mouse tooth germ time-lapse confocal | **Qualify** (see above) |
| SSBD [101](https://ssbd.riken.jp/repository/ssbd-repos-000101/) | SEM of mouse bio-hybrid implant tooth, 8 MB | Rejected: 2D SEM, not development |
| SSBD [105](https://ssbd.riken.jp/repository/ssbd-repos-000105/) | Canine CT, 333 KB | Rejected: dog, tiny |
| SSBD 318 | Yamamoto stem-cell project | Not tooth |
| Zenodo [8250595](https://zenodo.org/records/8250595) = Dryad [qnk98sfkk](https://doi.org/10.5061/dryad.qnk98sfkk) | RNAscope of human fetal tooth germ (22 files, 6.6 GB, CC0) | Rejected: human, 2D. Useful only if you also want human sections |
| Zenodo [17185791](https://zenodo.org/records/17185791) | Confocal of human dentin porosity | Rejected: human dentin, not development |
| Zenodo [11392406](https://zenodo.org/records/11392406), [10597292](https://zenodo.org/records/10597292), [8027553](https://zenodo.org/records/8027553); NKUT, STS-3D-Tooth, 3DTeethSegX, DentalDS | Clinical CBCT, X-ray and intraoral scans | Rejected: human clinical, not cellular |
| Mendeley [v3wgx8pm5y](https://data.mendeley.com/datasets/v3wgx8pm5y/1) | Human embryonic tooth germ scRNA-seq and spatial transcriptomics (two RData files) | Rejected: human, no images |
| GEO GSE53903, GSE162413, GSE255946, GSE320526, GSE221110 and ENA PRJNA681820, SRP058506, PRJNA643853, PRJNA274271, PRJNA480017, PRJNA595154, ERP144120 | Mouse (and cat, gecko) tooth RNA-seq or arrays | Rejected: sequencing. GSE79990, GSE189381 and GDS4453 were not read (rate limit) but are expression records by type |
| CellSeg3D, NIS3D, BioImage Archive, "NIH Dataset Catalog" | Generic tools or portals | Not tooth data; BioImage Archive searched earlier |
| UNSW Embryology, HEAL (Utah), histology-world, anatomicum, Sciencephoto, Alamy | Teaching figures and stock photos | Rejected: single illustrated images, rights unclear, no sections to stack |
| Papers: Coupling of angiogenesis and odontogenesis ([PMC8952600](https://pmc.ncbi.nlm.nih.gov/articles/PMC8952600/)), initiation knot ([PMC8126415](https://pmc.ncbi.nlm.nih.gov/articles/PMC8126415/)), peroxisomal dysfunction ([PMC11627416](https://pmc.ncbi.nlm.nih.gov/articles/PMC11627416/)), incisor niche actomyosin ([PMC12855154](https://pmc.ncbi.nlm.nih.gov/articles/PMC12855154/)), podoplanin ([PMC5319687](https://pmc.ncbi.nlm.nih.gov/articles/PMC5319687/)) | Mouse tooth imaging papers | No image deposit; the incisor paper points only to GEO GSE299463. Author requests only |
| Dryad [mgqnk98zf](https://doi.org/10.5061/dryad.mgqnk98zf), [12jm63xvn](https://doi.org/10.5061/dryad.12jm63xvn), [1g1jwsvc5](https://doi.org/10.5061/dryad.1g1jwsvc5) | ToothMaker simulations (4.8 GB), molar-shape CSVs, jaw RNA-seq FASTQ | Rejected: not images |
| FaceBase [B5-9848](https://doi.org/10.25550/b5-9848), [1-SXC4](https://doi.org/10.25550/1-sxc4), [1-77A8](https://doi.org/10.25550/1-77a8) | Adult incisor micro-CT; PN7-PN21 molar root micro-CT and H&E figures; published figure | Not early development; 1-SXC4 is a micro-CT plus histology overview that could be a 2D source for postnatal roots |
| Journal Figshare and SAGE collections (Usag-1/Bmp7, FAM20B, Msx1, Wnt10a, Cdc42 and others) | Supplementary figures attached to papers | Not datasets: single figure files |

### Second sweep on the task list (2026-10-06)

Seven tasks were run; every search was metadata only.

| Task | Result |
|---|---|
| Mendeley Data and OSF | Mendeley: only human embryonic tooth germ scRNA-seq and spatial data ([7ryrp25y6z](https://doi.org/10.17632/7ryrp25y6z), [mg3pw5mmd8](https://doi.org/10.17632/mg3pw5mmd8), [v3wgx8pm5y](https://doi.org/10.17632/v3wgx8pm5y)). OSF: only dentistry review protocols. The OSF title search for "tooth" and "molar" timed out, so it is not exhaustive. |
| Harvard Dataverse, Finnish and Japanese repositories | Dataverse DOIs (10.7910) returned nothing on tooth development through DataCite. Fairdata (Helsinki) and Japanese repositories are not indexed that way and were not searched directly. A DataCite search across all publishers found no further tooth image repositories beyond FaceBase, Zenodo, Dryad, Figshare, KCL and SSBD. |
| Section atlases | EMAP and eHistology (above). |
| Lab outputs (56 open-access papers from Jernvall, Tsuji, Morita, Green, Thesleff, Mikkola, Sharpe, Klein, Hu, Adameyko, Matalova and others) | No image deposits except the SSBD records already listed. One method paper is worth contacting the authors about, see below. |
| Europe PMC, wider screen (90 open-access mouse tooth imaging papers) | Only repository links already known; no new image data. |
| SSBD, IDR, BioImage Archive again | SSBD: 280 projects listed, only 98 and 100 are tooth image data. IDR: no tooth or jaw project except idr0144 (human jawbone histology). BioImage Archive: no tooth, jaw or organ-culture study. Cell Image Library was not searched. |
| Dryad loose ends | Closed above. |

**Best lead without public images: MORPHOVIEW** (Dev Dyn 2026, [10.1002/dvdy.70061](https://doi.org/10.1002/dvdy.70061), [PMC12818342](https://pmc.ncbi.nlm.nih.gov/articles/PMC12818342/)). It images mouse mandibular incisor tooth buds as 3D confocal volumes, with membrane-targeted fluorescent proteins and phalloidin, then segments individual cells with Cellpose; it also works on catshark and *Xenopus*. Code, MATLAB files and a Cellpose model (the file is named `CP_20241022_AllSharks.zip`; what it was trained on was not checked) are at [github.com/snoreis/MORPHOVIEW](https://github.com/snoreis/MORPHOVIEW) (BSD-3-Clause, about 24 MB). The paper's data statement does not name a repository for the image volumes, so this is a lead for asking the corresponding authors, not a dataset.

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

- Dryad datasets on mouse molar phenotypes (all four opened 2026-10-06, none are images): [10.5061/dryad.70585](https://doi.org/10.5061/dryad.70585) (BMP7 deletion: landmark files and 3D .ply meshes of adult molars, 37 MB), [10.5061/dryad.bm770](https://doi.org/10.5061/dryad.bm770) (third-molar size: one R data file), [10.5061/dryad.bt848](https://doi.org/10.5061/dryad.bt848) (craniofacial shape GWAS in a mouse hybrid zone: genotype and phenotype tables; this is not the molar-shape record an earlier note described) and [10.5061/dryad.f4qrfj6sn](https://doi.org/10.5061/dryad.f4qrfj6sn) (aging mice oral microbiome tables).
- FaceBase project [10.25550/9n-6d8m](https://doi.org/10.25550/9n-6d8m), amelogenin phosphorylation: the record describes developing enamel analyses, but whether image data are attached is unknown. A FaceBase search for micro-CT returns about 700 records (many are zebrafish); only the tooth-related ones were triaged above.
- Synchrotron (ESRF) mouse molar volume, [10.13140/rg.2.2.14729.03686](https://doi.org/10.13140/rg.2.2.14729.03686), a 2010 unpublished record.
- MorphoSource: filter by age or stage metadata to find juvenile specimens.

## Allen Institute for Cell Science image packages (2026-10-07)

The `allencell` Quilt bucket (35 packages, 146.7 TB, [catalogue](https://open.quiltdata.com/b/allencell)) was listed from the Quilt web page. Only the hiPSC single-cell dataset (now in README Section A) and Nuclear dataset 1 were opened; the rest are judged from package names and the [Allen download page](https://www.allencell.org/data-downloading.html), so treat their contents as unconfirmed. Terms of use for everything on allencell.org are noncommercial research use with citation ([terms](https://www.allencell.org/terms-of-use.html)); package pages were not checked for exceptions.

| Package | What is known | Open question |
|---|---|---|
| [`aics/nuclear_project_dataset_1`](https://open.quiltdata.com/b/allencell/packages/aics/nuclear_project_dataset_1) (also `_2`, `_3`, `_4`, not opened) | README read: single-cell 3D raw crops (3.1 TB) with 3D segmentations of cell (from the CellMask signal), DNA (NucBlue signal) and the tagged structure (19.8 GB); SON-mEGFP line plus other tagged nuclear lines, with some structures predicted by label-free models. Each file is one cell crop | Masks are per-cell crops, probably binary per file, not a labelled field of view; origin of the masks is signal-based segmentation, not manual |
| [`aics/hipsc_12x_overview_image_dataset`](https://open.quiltdata.com/b/allencell/packages/aics/hipsc_12x_overview_image_dataset) | Linked as the "12X colony overview dataset" on the Allen page | 12x is low magnification; not opened, probably not cellular resolution |
| `aics/hipsc_single_m1_cell_image_dataset`, `_m2_`, `_i1_`, `_i2_`, `_edge_`, `_nonedge_` | Listed in the bucket; look like subsets of the hiPSC single-cell dataset by cell-cycle stage or colony position | Not opened; likely redundant with the main package |
| [`aics/mitotic_annotation`](https://open.quiltdata.com/b/allencell/packages/aics/mitotic_annotation) | Training data for the mitotic-stage classifier, named in the main package README | Not opened |
| `aics/segmenter_model_zoo`, `aics/actk`, `aics/aics_mnist` | Models, toolkit and a benchmark set | Not opened |
| `aics/cell_culture_automation_dataset`, `aics/laminb1_sample_data`, `aics/average_morphed_cell_dataset_1` | Listed in the bucket | Not opened |
| [Label-free imaging collection](https://open.quiltdata.com/b/allencell/packages/aics/label-free-imaging-collection/tree/latest/) | The Allen page lists 3D transmitted-light and fluorescence image sets per structure (about 10 to 52 GB each) | Not opened; no cell labels mentioned |
| [Drug perturbation pilot](https://www.allencell.org/data-downloading.html#sectionDrugSignatureData) and [cardiomyocyte imaging](https://open.quiltdata.com/b/allencell/packages/aics/integrated_transcriptomics_structural_organization_hipsc_cm) | 3D `.ome.tif` image sets listed on the Allen page | Not opened; segmentations not mentioned |

## Leads

| Candidate | Source / link | What we know | Open question |
|---|---|---|---|
| 3DCellComposer outputs: 3D masks for HuBMAP 3D imaging mass cytometry and Allen hiPSC images | [Zenodo 12859553](https://zenodo.org/records/12859553) (CC-BY-4.0, 2024, Chen and Murphy; `segmentation_masks.zip` 11.5 GB + `evaluation_metrics.zip` 1.7 MB); paper [Methods 2025, 10.1016/j.ymeth.2025.07.007](https://doi.org/10.1016/j.ymeth.2025.07.007), [PMC13242829](https://pmc.ncbi.nlm.nih.gov/articles/PMC13242829/); code [github.com/murphygroup/3DCellComposer](https://github.com/murphygroup/3DCellComposer) and a [reproducible research archive](https://github.com/murphygroup/ChenMurphy3DCellComposerRRA) | The Zenodo record holds **masks only, no raw images**. The zip preview shows Python pickle (`.pkl`) files per image and per method (CellProfiler, 3DCellSeg and others, many matching thresholds) under `masks/IMC_3D/florida-3d-imc/...`, plus a binary image file. The paper says the masks are **pipeline outputs**: 2D segmentation models (DeepCell, Cellpose and others) assembled into 3D, scored by a no-human-annotation quality metric, so they are not ground truth. Source images, per the paper: three 3D imaging mass cytometry volumes (spleen, thymus, lymph node; 1 um in XY, 2 um in Z) from the HuBMAP portal (University of Florida Tissue Mapping Center), and 25 full-field 3D hiPSC culture images (membrane and nuclear channels plus one tagged structure) from the Allen Institute WTC-11 hiPSC Single-Cell Image Dataset ([Viana et al., Nature 2023](https://doi.org/10.1038/s41586-022-05563-7)) | Raw images must come from HuBMAP (dataset IDs are in the paper's Supplementary Table S2, not read) and the Allen hiPSC dataset (now in README Section A under Allen Institute terms of use); HuBMAP access terms were not checked. Pickles should only be loaded from a source you trust. Does not meet Section A as ground truth; may still serve as predicted masks to compare against |
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
