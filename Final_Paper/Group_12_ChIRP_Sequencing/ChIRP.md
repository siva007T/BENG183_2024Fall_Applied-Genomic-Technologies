# ChIRP-Seq: Chromatin Isolation by RNA Purification Sequencing
- Haley Fernandez
- Itai Lavi
- Nir Reitner

## Table of Contents
- [What is ChIRP-seq?](#what-is-chirp-seq)
- [Applications of ChIRP-Seq](#applications-of-chirp-seq)
- [Case Study: "Exploration and bioinformatic prediction for profile of mRNA bound to circular RNA BTBD7_hsa_circ_0000563 in coronary artery disease"](#case-study-exploration-and-bioinformatic-prediction-for-profile-of-mrna-bound-to-circular-rna-btbd7_hsa_circ_0000563-in-coronary-artery-disease)

# What is ChIRP-seq?

## Quick Refresher on ChIP-seq:
**Chromatin Immunoprecipitation Sequencing**, or **ChIP-Seq** is a biological research method that utalizes chromatin immunoprecipitation and high-throuput DNA sequencing in order to **identify the binding sites of DNA-associated proteins** across the genome. For example, some proteins that may be targted in a ChIP-seq include transcription factors or histones. This method is often applied in order to study gene regulation, epigenetic modifications, and protein-DNA interactions.

### Steps of ChIP-seq:
1. **Cross-linking**: Cells are chemically trated to crosslink proteins to DNA, fixing and preserving the protein-DNA molecules.
2. **Chromatin Fragmentation**: The Chromatin-RNA complexes are is broken up into smaller fragments, usually through sonication or enzymatic digestion.
3. **Immunoprecipitation**: An antibody specific to the target protein is designed and sent in to pull down on the protein-DNA complexes.
4. **Reversal of Crosslinks**: The proteins are washed off, leaving the isolated chromatin DNA.
5. **Library Preparation and Sequencing**: These DNA fragments are prepared into a sequencing library and then undergo high-throughput sequencing.
6. **Data Analysis**: Sequencing reads are mapped and alignrd back to a reference genome, and peaks are identified to signify the locations of protein-DNA interaction sites.
#### ChIP-seq Workflow:
<img src="chip-protocol-steps.png" alt="ChIP-seq Workflow" width="350">

---

## What is ChIRP-seq?
**Chromatin Isolation by RNA Purification Sequencing,**, or **ChIRP-seq** is a very similar method to ChIP-seq but is used to analyze **RNA-DNA interactions** across the genome rather then protein-DNA interactions. This technique identifies binding sites of specific RNAs, such as long noncoding RNAs (lncRNAs), sending probes to pull down on DNA-bound RNA molecules, dragging the DNA and their associated chromatin complexes along with them. This is then followed by DNA sequencing in order to identify the targeted DNA and align the locations of these DNA-RnA complexes. It is often used to gain insights into how RNA molecules are involved in genomic actions such as regulating gene expression and chromatin architecture.

### Steps of ChIRP-seq:
1. **RNA Capture**: Specific biotin-labeled probes are designed to bind and hybridize to the target RNA molecules.
2. **Chromatin Isolation**: Crosslinked chromatin complexes are fragmented, using sonfication or enzymes.
3. **Pulldown**: The RNA-probe complexes, along with its associated DNA and proteins, are captured using magnetic streptavidin beads.
4. **DNA Purification**: RNA is washed off, isolating the purifed DNA.
5. **Sequencing and Analysis**: Isolated DNA is sequenced, and the reads are mapped back the genome to identify RNA-DNA interaction sites.
#### ChIRP-seq Workflow:
<img src="ChIRP-Workflow.png" alt="ChIP-seq Workflow" width="300">

---

# Applications of ChIRP-seq

**RNA-DNA** interactions are not well known or understood, and have only recently been studied thanks to ChIRP-seq. This research has uncovered the dynamic role of long noncoding RNAs (lncRNAs) in regulating gene expression. ChIRP-seq is a general-purpose tool for studying lncRNAs, along with other DNA-binding RNAs, allowing RNA-DNA interactions to be studied anywhere on the genome. So far, these studies have uncovered some key genes where these lncRNAs have an important role.

### Developmental Genes

Developmental genes are, as their name would suggest, involved in the growth and development of animal bodies. As such, they are primarily expressed in stem cells. These genes have two major roles: 
1. Tissue Formation: Developmental genes are responsible for building up the body's tissues and organs. During adolescence, they trigger cell proliferation in response to hormonal changes. Throughout the organism's lifetime, they replace old cells with new cells, and repair cuts, wounds, and other tissue damage.
2. Cell Differentiation: Stem cells must differentiate into the different cell types in the body, in correct proportions and at the right frequency. During pregnancy, the zygote grows into an embryo of stem cells, which then differentiate through multiple rounds of division into organ- and tissue-specific stem cells. Even in adulthood, multipotent stem cells are present which are specific to a certain tissue but can generate a variety of cells within those bounds. One example which is particularly studied with ChIRP-seq is Hematopoetic Stem Cells (HSCs), which are found in bone marrow and can differentiate into any type of blood cell, including red blood cells, white blood cells (immune cells) and platelets.

Many interactions between lncRNAs and developmental genes have been discovered in the past decades, especially in HSCs. Studies have discovered their effects in some key genes involved in blood cell production. Here are two lncRNAs whose role in regulating blood cell expression was unknown, until ChIRP-seq revealed their interaction with key developmental genes.

### The Beta-Globin Gene

The beta-globin gene produces one of the subunits of hemoglobin, the protein responsible for red blood cell's ability to carry oxygen through the blood.  Using ChIRP-seq, researchers discovered that a certain lncRNA called ERV-9, a product of the ERV-9 LTR retrotransposon, has a function in regulating the beta-globin gene in humans, but not in mice.*

ChiRP-seq for lncRNA ERV-9 on the Beta-Globin Gene in Mouse and Human cells.
<img src="globin.png" alt="ChIRP-seq on Beta-Globin gene in mouse and human">

This revealed a high degree of binding in the human beta-globin gene but not in the mouse beta-globin gene. Further experiments indicated that the absence of ERV-9 inhibits beta-globin expression, confirming that this interaction regulates the expression of the gene.

*Long non-coding RNAs transcribed by ERV-9 LTR retrotransposon act in cis to modulate long-range LTR enhancer function
https://academic.oup.com/nar/article/45/8/4479/2962182

### The Itpkb Gene

The Itpkb gene causes HSCs to differentiate into a certain type of T-cell lymphocyte. ChIRP-seq found that lncHSC-2 binds close to the transcription start site of this gene.** 

ChIRP-seq on the Iptkb Gene and Other Genomic Information
<img src="itpkb.png" alt="ChIRP-seq on the Iptkb gene">

Because it binds so close to the transcription start site, it's thought that lncHSC-2 has a role in regulating Itpkb and lymphocyte differentiation. This could only have been discovered using ChIRP-seq, since it was a previously unknown lncRNA and interaction.

**Long Non-coding RNAs Control Hematopoietic Stem Cell Function
https://pmc.ncbi.nlm.nih.gov/articles/PMC4388783/

---

## Case Study: "Exploration and bioinformatic prediction for profile of mRNA bound to circular RNA BTBD7_hsa_circ_0000563 in coronary artery disease"

This case explored the bioinformatic prediction for the profile of mRNA bound to the circular RNA BTBD7_hsa_circ_0000563. Using an alternative approach, ChIRP-sequencing was used to interrogate these ribonucleoprotein complexes and subsequently employ functional assays to explore how these candidate mRNAs directly impact the disease process. This led to the identification of 221 mRNAs that bound the circular RNA. This case study highlights the power of ChIRP-sequencing to investigate RNA-mediated regulatory networks and downstream pathway effects in association with CAD.

### Key Findings:
1. **Objective**: To investigate the role of the circular RNA BTBD7_hsa_circ_0000563 in coronary artery disease by identifying mRNAs bound to it and analyzing their functional significance in disease progression.
2. **Methodology**:
   - ChIRP-sequencing was used to isolate RNA-chromatin complexes and analyze their regulatory potential.
   - Bioinformatic tools and functional assays identified 221 mRNAs interacting with the circular RNA, showcasing its impact on RNA-mediated regulatory networks.
3. **Visual Data**:
   - **Heatmap**: Highlights clear expression differences between the target and control groups, validating the isolation of specific RNA-binding partners.
   - **Volcano Plot**: Quantifies significantly upregulated mRNAs, providing evidence of RNA-mediated transcriptional regulation.
4. **Impact**:
   - Demonstrates the utility of ChIRP-sequencing in studying RNA-mediated regulatory mechanisms in diseases like CAD.
   - Highlights the role of circular RNAs in regulating downstream pathways and their impact on disease progression.

### Figures:
*Figure 2*: 
![Figure 2: Heatmap and Volcano Plot](figure2.png)

- Figure 2 shows the differentially expressed genes identified through the ChIRP-Seq. The heatmap provides a qualitative outlook on the RNA binding, the volcano plot shows the quantitative data of the experiment. 
1. **Heatmap**:
   - Visualizes expression differences between BTBD7 circular RNA and control groups.
   - Shows the relative expression levels of mRNAs that were captured by the ChIRP-Seq assay in the target group
   - Each column represents the individual conditions while the rows correspond to a certain gene
   - The red symbolizes upregulation while the blue symbolizes downregulation which is indicative of how much of these mRNAs are present
   - Confirms the successful isolation of RNA-chromatin complexes with minimized background noise.
2. **Volcano Plot**:
   - Displays a subset of significantly upregulated mRNAs among 221 identified targets.
   - P-value is the statistical significance shown compared to the log2 fold changes (magnitude of expression change) for mRNAs
   - On the x-axis, you can see the log2FC (Log2 fold changes) which shows either the upregulation (right) or the downregulation (left) in the target group compared to the control group
   - On the y-axis, it is the -log10P which is representative of the statistical significance of the change
   - Provides quantitative evidence of the circular RNA’s regulatory role in coronary artery disease.

### Implications:
This case study highlights the potential of ChIRP-sequencing in unraveling RNA-mediated regulatory mechanisms. By mapping RNA-chromatin interactions and analyzing their role in regulating gene expression and chromatin dynamics, we are closer to understanding the mechanisms behind diseases and their progression.

*"Exploration and bioinformatic prediction for profile of mRNA bound to circular RNA BTBD7_hsa_circ_0000563 in coronary artery disease"* [(https://doi.org/10.1186/s12872-024-03711-7)](https://doi.org/10.1186/s12872-024-03711-7).

---

# References
- [Illumina Sequencing Method Explorer - ChIRP-seq](https://www.illumina.com/science/sequencing-method-explorer/kits-and-arrays/chirp-seq.html)
- Guo, N., Zhou, H., Zhang, Q. et al. Exploration and bioinformatic prediction for profile of mRNA bound to circular RNA BTBD7_hsa_circ_0000563 in coronary artery disease. BMC Cardiovasc Disord 24, 71 (2024). https://doi.org/10.1186/s12872-024-03711-7
