# Tharun Kumar J

### _Computational Biology | Bioinformatics Pipelines | Long-read Genomics | Machine Learning_

📍 Hosur, Tamil Nadu, India · ✉️ [tharunjayy@gmail.com](mailto:tharunjayy@gmail.com) · ☎️ +91 94863 47125  
🔗 [LinkedIn](https://www.linkedin.com/in/tharunjay) · [GitHub](https://github.com/TharunkumarJayakumar)

[Jump to: Skills](#-technical-skills) · [Experience](#-experience) · [Education](#-education) · [Projects](#-selected-projects) · [Publications](#-publications) · [Contact](#-contact)

---

#### Profile

M.Tech Biotechnology graduate (2026) with ~1 year of R&D experience in primer and assay design, bioinformatics, genomic and transcriptomic data analysis, pharmacogenomics, multi-omics integration, and reproducible pipeline development. Experienced in benchmarking tools and in building, validating and deploying NGS pipelines for repeat disorders, TB AMR detection, viral genomics, mitochondrial genomics, transcriptomics and pharmacogenomics. Strong proficiency in Bash, R and Python, with hands-on machine learning on biological data.

**Target role:** Scientist / Computational Biology — pipeline development, genomic data analysis and applied machine learning.

---

## 🔬 Technical Skills

**Programming & data analysis**
- **R:** DESeq2, edgeR, limma, ggplot2, Seurat, phyloseq, vegan, clusterProfiler, Shiny app development
- **Python:** NumPy, pandas, SciPy, scikit-learn, matplotlib, seaborn, Biopython, SHAP, CTGAN/SDV
- **Bash/Linux:** shell scripting, Conda environment management, HPC job submission, Git/GitHub

**Pipeline development & bioinformatics engineering**
- **Nextflow DSL2:** modular pipeline design, subworkflows, Docker/Singularity containerization, JSON-based configuration, HPC/server execution
- **Long-read NGS (ONT):** Minimap2, Medaka, Porechop, Dorado, Guppy, Nextclade, Straglr, wf-human-variation, Clair3
- **Variant analysis:** BCFtools, GATK HaplotypeCaller, FreeBayes, Snippy, SnpEff, VEP, SAMtools, BEDtools, Mosdepth
- **Assembly & metagenomics:** Flye, SPAdes, MetaBAT2, MaxBin2, DAS Tool, CheckM, GTDB, AMRFinderPlus, ABRicate, GeNomad, Krona, Anvi'o, Kraken2

**Transcriptomics & multi-omics**
- RNA-seq: STAR, HISAT2, featureCounts, HTSeq, Salmon, DESeq2, edgeR, StringTie; GO/KEGG enrichment with g:Profiler and clusterProfiler
- Epigenomics: ChIP-seq (MACS2, deepTools, MEME), ATAC-seq (Bowtie2, Picard, pyGenomeTracks), bisulfite-seq (bwa-meth, MethylDackel)
- Network/comparative: Cytoscape STRING + MCODE, Roary, RAxML, QIIME, phyloseq

**Primer & assay design**
- Primer3, PrimerJinn, PrimerPooler; multiplex and allele-specific panels, delta-G-aware cross-dimer filtering, adaptive-sampling panels, MAFFT alignment checks

**Structural & molecular bioinformatics**
- SWISS-MODEL, AlphaFold structure analysis, CB-Dock 2, 1-Click Docking, CB Dock 2, molecular dynamics, Augustus gene prediction
- Databases: NCBI, UniProt, PDB, KEGG, GEO, SRA, miRBase, HMDD, TargetScan, Pfam, InterPro, CATH, SCOP

**Machine learning**
- Supervised models: SVR, GBM, Random Forest, Ridge, Linear Regression; LOOCV benchmarking
- Generative augmentation with CTGAN; explainable AI with SHAP; biomarker discovery and risk prediction from omics data

---

## 💼 Experience

### Junior Scientific Analyst — R&D Bioinformatics
**Genotypic Technology Pvt Ltd, Bengaluru** · _Jun 2026 – Present_

- **Primer & assay design:** Designing multiplex primer panels for nanopore amplicon sequencing and adaptive sampling using Primer3, PrimerJinn and PrimerPooler; applied Tm/GC, hairpin, self-dimer, allele-specific and delta-G cross-extension constraints with custom i5/i7 barcode indexing. Delivered a multi-chromosome SNP-detection panel and a mitochondrial genome amplicon panel; verified binding sites with MAFFT and reported amplicon size, coverage and primer-binding statistics.
- **R&D approach:** For each project, performed literature and tool review, shortlisted and benchmarked tools on real and simulated datasets, selected best-performing methods, defined pipeline routes, then built, validated and deployed workflows as containerized Nextflow pipelines. Validation included sensitivity, specificity and concordance against published/reference results.
- **STR expansion genotyping pipeline:** Independently built and containerized a Nextflow DSL2 pipeline for SCA, FMR1 and HTT repeat expansions from ONT amplicon reads: Porechop/Dorado trimming, quality/length filtering, minimap2 alignment, Clair3 calling on a custom repetitive-region model, haplotagging, per-haplotype repeat sizing, and automated R Markdown reports with normal/intermediate/premutation/full-expansion classification. Benchmarked against Straglr, STRime/STRDime, Nanorepeat, Stripy, Stranger and EPI2ME wf-human-variation; reconciled allele lengths against literature/EPI2ME references and corrected locus-specific BED coordinates and caller parameters.
- **ONT trimming & QC benchmark:** Compared Porechop, Dorado SUP basecalling-with-trimming and Cutadapt on amplicon and mitochondrial datasets; quantified Q-scores, N50, read-length distributions, per-target depth with Mosdepth and allele concordance in IGV; delivered companion statistics and figure reports.
- **TB genomics & AMR catalogue (WHO 2023):** Analysed clinical *M. tuberculosis* ONT datasets across sequencing batches against custom target-region sets. Built a Python parser for the WHO 2023 AMR catalogue, corrected mis-graded ASSOC-w-R / R-interim categories, and reconciled variants against pipeline BED files into multi-sample Excel stratification reports. Evaluated a custom TB-Profiler database (rules.yml + mutations.json; 73-gene coverage/confidence), cross-checked resistance calls against WHO-2023 inference, and ran Kraken2/Krona plus IS6110/IS1081 contamination checks.
- **UMI low-VAF variant calling:** Developed a Nextflow UMI consensus pipeline for ONT amplicons: adapter/UMI identification, paired-read merging, edit-distance clustering, PCR-duplicate/error suppression, consensus generation and FreeBayes calling. Validated on staged in-silico bundles including PCR imbalance, substitution/indel/truncation errors, UMI errors and 10%→5% VAF dilution; reproducible detection down to ~5% VAF.
- **Pharmacogenomics (CYP2D6):** Performed star-allele haplotyping and metabolizer phenotype assignment from ONT amplicons; cross-validated PyPGx, Stargazer, Aldy, Cyrius, SpecImmune and CoLoRGen on GRCh37; built synthetic PharmVar-based panels and produced multi-tool diplotype/phenotype concordance matrices and HTML reports.
- **Mitochondrial workflow:** Developed and validated an ONT amplicon mitochondrial workflow (Porechop, minimap2, SAMtools, Clair3, SnpEff, haplogrep3, mutserve) for homoplasmy/heteroplasmy calling and haplogroup assignment; benchmarked against synthetic panels and published references.
- **Viral genomics:** Built RSV-A/RSV-B workflows and HIV drug-resistance/lineage workflows on synthetic and public nanopore data; performed MSA, identity matrices and BLAST/tBLASTx comparisons across JEV, WNV, YFV, Zika and SARS-CoV-2.
- **Platform integration:** Containerized and deployed STR, TB/AMR-Krona, UMI consensus and EPI2ME integration pipelines on an in-house AI-assisted orchestration platform; profiled output consistency and resource behaviour and logged structured defect reports for product engineering.
- **Simulation-based validation:** Validated a TB variant-calling pipeline with badread-simulated ONT reads spiked with catalogue mutations; computed TP/TN/FP, sensitivity, specificity and precision across repeated runs.
- **Internal R&D conference:** Prepared live Ubuntu/VM demo environments and demonstrated in-house pipelines to internal teams.

### Project Intern — R&D Bioinformatics
**Genotypic Technology Pvt Ltd, Bengaluru** · _Dec 2025 – May 2026_  
_Reporting manager: Dr. Prakruthi, Senior Scientist – R&D_

- Built and validated modular Nextflow DSL2 pipelines for AMR detection, variant annotation, viral genomics (RSV) and bulk RNA-seq.
- Integrated Nextclade for RSV clade/subtype classification and validated on Oxford Nanopore data.
- Built and validated an ABO blood-typing pipeline from clinical sequencing samples, producing branded Excel reports with coverage metrics and citations.
- Developed a *Salmonella Typhi* AMR pipeline combining ABRicate, Kraken2, KrakenTools, Krona, GeNomad and AMRFinderPlus in Nextflow DSL2.
- Performed SCA STR expansion analysis with wf-human-variation (Straglr module), Singularity containers and custom locus BED files; automated batch processing across barcoded samples with Bash.
- Automated bulk RNA-seq with STAR, featureCounts and DESeq2 for *Mus musculus* paired-end Illumina data; debugged module errors and optimized processing.
- Contributed to in-house AI-assisted genomics platform alpha testing: executed diagnostic-panel and pipeline workflows on internal datasets, assessed execution behaviour, output consistency and performance, and documented workflow failures, annotation inconsistencies and module-level errors.
- Performed end-to-end metagenomic assembly and binning (Flye → MetaBAT2/MaxBin2 → DAS Tool) on public ONT human-gut datasets, generating MAGs validated with CheckM and GTDB; ran Anvi'o pangenome analysis, functional enrichment, pathway reconstruction and ANI calculations.
- Supported WGS variant analysis for an MTB genomics R&D initiative and resolved RAM/file-size constraints for large MAFFT alignments via server execution.

### Project Intern
**DRDO Industry Academia Centre of Excellence, BU Campus, Coimbatore** · _Jan 2024 – Aug 2024_

- Worked on “Toxicity Effect of Ferrocene on Early Life Stages of Zebrafish (*Danio rerio*): A Multi-Biomarker Approach.”
- Assessed acute ferrocene toxicity in zebrafish embryos using biochemical, enzymatic, neurotoxicological and histopathological assays; demonstrated dose-dependent toxicity with aquatic-ecosystem relevance.

### Intern Trainee
**DRDO-BU Center for Life Sciences, Coimbatore** · _Aug 2023_

- 15-day training on nanomaterial synthesis and biological applications.
- Operated SEM, fluorescence microscopy, BET, DLS and zeta-potential instruments for nanoparticle characterization.

### Intern Trainee
**MAIVA Pharma Pvt Ltd, Hosur** · _Oct 2022_

- Two-week rotation across QC (chemical & microbiology), production, QA and supply chain under GMP.
- Observed HPLC, GC, GC–MS, LC–MS, ICP–MS and WFI purification systems.

### Intern Trainee
**VINSMILE Pharma Manufacturer & Distribution, Kallakurichi** · _Mar 2022_

- Two-week exposure to formulation and packaging of tablets, creams, ointments, capsules and shampoos.
- Observed GMP documentation, primary/secondary packing, QA measures and pharmaceutical production machinery.

---

## 🎓 Education

- **M.Tech**, Biotechnology | PSG College of Technology, Coimbatore · _2024–2026_
- **B.Tech**, Pharmaceutical Technology | Hindusthan Institute of Technology, Coimbatore · _2020–2024_, **88.5%**
- **HSC**, PCMB | Tamil Nadu Board of Secondary Education · _2020_, 69%
- **SSLC** | Tamil Nadu Matriculation Board · _2018_, 82%

---

## 🚀 Selected Projects

**Modular AMR analysis pipeline from NGS data** — _M.Tech major project, ongoing_  
Nextflow DSL2 workflow integrating Fastp/Porechop QC, SPAdes/Flye assembly, Minimap2 alignment, RGI-CARD AMR detection, GeNomad mobile-element detection, Kraken2/Krona taxonomy and Bakta annotation for Illumina and ONT data; validated on clinical isolate datasets.

**Explainable ML with generative augmentation for hydrogen production** — _submitted for publication_  
Built an 83-observation MEC dataset, expanded to 583 with CTGAN, benchmarked SVR/GBM/RF/Ridge/Linear Regression using LOOCV (best SVR **R² = 0.659**), and used SHAP to identify current density as the dominant predictor of hydrogen production rate. Tools: Python, scikit-learn, SDV, SHAP, pandas, matplotlib.

**Predictive modelling of gene signatures in Type II Diabetes Mellitus**  
Integrated RNA-seq and microarray data to identify 31 hub genes; performed GO enrichment, built ML risk-prediction models and deployed an interactive Shiny app. Presented at PSG Tech International Conference (ISBN 978-93-95105-97-2).

**In-silico vaccine design against HIV-2**  
Designed a multi-epitope vaccine candidate against conserved HIV-2 regions using IEDB/UniProt; screened epitopes for antigenicity and allergenicity and constructed adjuvant-linked vaccine models.

**Molecular docking and MD simulation of *Macrotyloma uniflorum* phytochemicals**  
Docked 30 phytochemicals against P-glycoprotein and MRP3 targets using 1-Click Docking, CB-Dock 2 and MD simulations; highlighted rutaecarpine as a promising P-gp inhibitor.

**Ferrocene toxicity in zebrafish** — see Experience (DIA CoE, 2024).

**Public repository:** [vcf-annotate-smk](https://github.com/TharunkumarJayakumar/vcf-annotate-smk) — reproducible GRCh38 VCF filtering and annotation workflow using Ensembl VEP and bcftools, with continuous integration.

---

## 📜 Publication

Subramaniapillai Niju, Jayakumar Tharunkumar, Perumal Asaithambi. “Determinants of Hydrogen Production in Microbial Electrolysis Cells: Microbial, Electrochemical and Operational Perspectives.” *Sustainable Chemistry One World*, Elsevier, Vol. 100234, 2026. [https://doi.org/10.1016/j.scowo.2026.100234](https://doi.org/10.1016/j.scowo.2026.100234) — _In Press_.

---

## 🎤 Conferences & Workshops

- International Conference on “Advances in Molecular Medicine and Multi Omics Technology,” PSG Tech, Coimbatore — _20 Sep 2025_. Presented “Predictive Modelling of Gene Signatures in Type II Diabetes Mellitus and their Functional Validation” (ISBN 978-93-95105-97-2).
- National Level Technical Symposium, Dhanalakshmi Srinivasan Engineering College, Perambalur — _22 Sep 2023_. Presented “Evaluation of anti-hyperglycemic activities of *Borassus flabellifer* leaf extract” and “In-silico vaccine designing against HIV-2.”
- YUKTI Innovation Challenge 2023, IIC, Ministry of Education’s Innovation Cell — “Biodegradable Polymers: A Smart Strategy for Replacing Blister Packages.”
- Internal Smart India Hackathon 2023 — “Bio-diesel Production from Waste Cooking Oil using Catalyst from a Novel Source.”
- Internal Smart India Hackathon 2022 — “Refined Solution to help Cities locate EV Charging Infrastructure” and “LSC Integrated Cell-based Disease Detection.”
- Two-day workshop on “Homology Modeling, Active Site Prediction and Docking: From Theory to Application,” Discovery Boulevard — _2025_.
- Two-day workshop on “Futuristic R&D Endeavours on Soldier Support Technologies,” DIA CoE, BU — _2024_.
- Certification in Molecular Docking, BIOGrademy — _2023_.
- One-day workshop on “Medical Equipment Troubleshooting,” Karpagam University — _2023_.
- Two-day virtual workshop on “Optimization of Process Parameters using MINITAB,” BIT — _2022_.
- NPTEL Entrepreneurship Essentials — _2022_.
- Two-day National workshop on “Analytic Techniques used in Nanotechnology,” ISBM Uni — _2021_.
- One-day workshop on “Fighting Covid-19 using 3D Printing Technology,” HIT — _2021_.

---

## 🏆 Achievements

- Winner — Best Project Expo 2024 (eco-friendly pharmaceutical packaging material).
- Winner — Technical Quiz (Azooka) and Photography/Poster Presentation (“Nurturing the Nature”).
- Runner-up — Intra-college Poetry Competition.
- Activities: running, cycling, volleyball, photography and reading.

---

## 📞 Contact

**Tharun Kumar J**  
Hosur, Tamil Nadu, India  
[tharunjayy@gmail.com](mailto:tharunjayy@gmail.com) · +91 94863 47125  
[LinkedIn](https://www.linkedin.com/in/tharunjay) · [GitHub](https://github.com/TharunkumarJayakumar)

_References available on request._
