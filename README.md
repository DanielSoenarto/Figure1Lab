# Figure 1 Lab
This is an internship emulator by [Dean Lee](https://github.com/deanslee/FigureOneLab): [F1L on Linkedin](https://www.linkedin.com/pulse/introducing-f1l-internship-emulator-dean-lee-xckee/?trackingId=OSGSU27GSGG2casuU42SFA%3D%3D)

# Week 1
Key scientific question (KSQ): How can we use the available scRNA-seq data from cancer cell lines whether these cancers are treatable using Trastuzumab and Bevacizumab?

## What is scRNA-seq?
A process to sequence the collective mRNAs (transcriptome) of a single cell, whose expression correlates well with cellular traits and changes in cellular state (Haque et al., 2017).

## Why do we need scRNA-seq in the first place?
Almost every cell in heterogeneous multicellular organisms such as humans has the same genetic material. But, why do cells in every part of the human body are different with each other? This is due to gene expression that is responsible to turn on or off which genes in each cell, which we can observe by studying each cell's transcriptome. Some applications include understanding the initiation of tumours and pathogenesis of COVID-19 infection (Jovic et al., 2022).

## What are cancer cell lines?
These are _in vitro_ model systems used in cancer research and drug discovery. If maintained under the right conditions and controls, these cell lines retain most of the genetic properties of the cancer of origin (Mirabelli et al., 2019). 

## How does Trastuzumab target HER2 (mechanism of action)?
Breast cancer patients have overexpression and amplification of HER2 (human epidermal growth factor receptor 2) gene, which encodes for the transmembrane tyrosine kinase receptor that is responsible for stimulating growth factor signaling pathways (cell division and cell growth). Hence, it serves as an oncogenic driver in breast cancer. The trastuzumab antibody binds to the juxtamembrane domain of HER2 which downregulates the expression of HER2 and causes downregulation of PI3K pathway signaling and downstream mediators of cell cycle progression such as cyclin D1 (Gajria & Chandarlapaty, 2011). This drug also works for HER2-positive gastric cancer (Shitara et al., 2020).

## How does Bevacizumab target VEGF (mechanism of action)?
Vascular endothelial growth factor A (VEGF) is a growth factor that stimulates the growth and survival of endothelial cells in blood vessels. Since cancer cells demand for oxygen and nutrients, they can promote angiogenesis (formation of new capillaries out of existing blood vessels) under hypoxia condition (no or low level of oxygen). Then, hypoxia inducible factor (HIF) binds to the hypoxia response element present in the VEGF gene, thus inducing the transcription of VEGF protein. To inhibit blood supply to tumour tissues and prevent growth of tumour blood vessels, Bevacizumab acts by selectively binding circulating VEGF (Kazazi-Hyseni et al., 2010).

## Unclear KSQ: How to explore the potential use of both Trastuzumab and Bevacizumab to treat cancers using scRNA-seq data?
Since both drugs are specific and selective, probably these 2 drugs can only be used to treat other cancers that are either HER2-positive or VEGF-positive?

# Week 2
## Overview
The main paper of this F1L internship emulator as reference (Kinker et al., 2020).

### What did the authors do?
They investigated whether cancer cell lines maintain cellular heterogeneity and plasticity, which are the main characteristics of human tumors that play critical role in disease progression and treatment failure. To do this, they utilized scRNA-seq since initial studies have shown expression patterns of intra-tumoral heterogeneity (ITH). Ultimately, they examined whether these cancer cell lines could recapitulate ITH programs by using cell lines from the Cancer Cell Line Encyclopedia (CCLE) collection.

### Why did they do it?
Even though cell lines are the main workhorse in cancer research, it is still unclear whether they can recapitulate the cellular heterogeneity observed among malignant cells in tumors. Ideally, these cell lines as models should have almost the same charactersitics such as tumors cells. Even though initial studies have proven expression patterns of ITH, it was still unclear on how the mechanisms and functional implications of this cell lines were.

### What did they learn?
After profiling around 200 cancer cell lines from 22 cancer types, they found 12 expression programs that are recurrently heterogeneous (RHPs) within many cancer cell lines. There were 2 of these programs associated with cell cycle and the rest of them with diverse biological processes. They learned that 9 of these programs in those cell lines were also observed in human tumors, which they were focusing on as model systems of cellular heterogeneity. Their study also showed that multiple RHPs are of potential clinical relevance since these subpopulations demonstrated unique drug responses. Overall, they identified recurrent patterns of heterogeneity that are shared between tumors and specific cell lines.

## Questions for Testing My Understanding

### How did the authors handle the potential caveat of co-culturing cell lines before profiling by scRNA-seq? Why do you think that caveat was or was not adequately addressed?
Their analysis suggested that co-culturing had a minor effect on cells heterogeneity for each cell line as the heterogeneity patterns were similar between cell lines from the same pool as between cell lines of different pools. They also did a controlled experiment of profiling six cell lines with and without co-cuturing which modestly affected average gene expression in each cell line, but patterns of heterogeneity were consistent between 2 conditions. 

Since the focus of this work was to examine the ability of cancer cell lines to recapitulate ITH programs, which includes cell heterogeneity and plasticity, they should have ensured that no co-culturing effects can reduce heterogeneity of each cells in each pools. I think this caveat was adequately addressed, but maybe only to some extent (I speculated that maybe co-culturing gave rise to discrete subpopulations in a few cell lines). 

### The authors identified discrete subpopulations of cells within a subset of individual cell lines (Fig. 2A-B). What might be the reason why some cell lines have these discrete subpopulations while others do not?
They identified extensive variability of gene expression across cells within individual cell lines, including discrete subpopulations of cells and continuous patterns that reflect spectra of cellular states. The reason why some cell lines have discrete subpopulations might be due to the effect of co-culturing. Study from Vis et al. (2020) showed an increase in complexity can be accomplished by culturing different cell types together in one culture (co-culturing). Direct co-cultures facilitate physical contact between the different cell types which allows for communication though their surface receptors.

### What are Recurrent Heterogeneous Programs (RHPs) and how were they defined?
Recurrent heterogenous programs (RHPs) are patterns of gene expressions or processes in molecular level that are repeatedly seen across different cell lines.
 
There were two most prominent RHPs that reflected the cell cycle and the other 10 RHPS reflect other cellular processes not associated with the cell cycle. They defined these RHPs by hierarchical clustering of the NMF programs based on their shared genes and for the other 10 RPHs by functional enrichment of their signature genes, by the cell lines in which they are observed, and by their potential regulators.

### How do the identified RHPs relate to _in vivo_ programs of heterogeneity in tumors, and what evidence supports this relationship?
The relation was that they found 7 out of the 10 cell line RHPs are highly similar to the _in vivo_ RHPs, as defined by highly significant overlap of signature genes, through statistical methods such as FDR-adjusted p value and Jaccard index correlation plots. They further supported this finding through analysis of both melanoma and HNSCC cells from cell lines and tumors.

### Where can you download the scRNA-seq data as shown in Figure 1B?
The scRNA-seq data in Figure 1B can be downloaded from the Broad Institute’s single cell portal (SCP542) at https://singlecell.broadinstitute.org/single_cell/study/SCP542/pan-cancer-cell-line-heterogeneity#study-download

## References
Gajria, D., & Chandarlapaty, S. (2011). HER2-amplified breast cancer: mechanisms of trastuzumab resistance and novel targeted therapies. Expert Review of Anticancer Therapy, 11(2), 263–275. https://doi.org/10.1586/era.10.226

Haque, A., Engel, J., Teichmann, S. A., & Lönnberg, T. (2017). A practical guide to single-cell RNA-sequencing for biomedical research and clinical applications. Genome Medicine, 9(1). https://doi.org/10.1186/s13073-017-0467-4

Jovic, D., Liang, X., Zeng, H., Lin, L., Xu, F., & Luo, Y. (2022). Single‐cell RNA sequencing technologies and applications: A brief overview. Clinical and Translational Medicine, 12(3). https://doi.org/10.1002/ctm2.694

Kazazi-Hyseni, F., Beijnen, J. H., & Schellens, J. H. (2010). Bevacizumab. The oncologist, 15(8), 819–825. https://doi.org/10.1634/theoncologist.2009-0317

Mirabelli, P., Coppola, L., & Salvatore, M. (2019). Cancer Cell Lines Are Useful Model Systems for Medical Research. Cancers, 11(8), 1098. https://doi.org/10.3390/cancers11081098

Kinker, G. S., Greenwald, A. C., Tal, R., Orlova, Z., Cuoco, M. S., McFarland, J. M., Warren, A., Rodman, C., Roth, J. A., Bender, S. A., Kumar, B., Rocco, J. W., Fernandes, P. A. C. M., Mader, C. C., Keren-Shaul, H., Plotnikov, A., Barr, H., Tsherniak, A., Rozenblatt-Rosen, O., Krizhanovsky, V., … Tirosh, I. (2020). Pan-cancer single-cell RNA-seq identifies recurring programs of cellular heterogeneity. Nature genetics, 52(11), 1208–1218. https://doi.org/10.1038/s41588-020-00726-6

Shitara, K., Bang, Y., Iwasa, S., Sugimoto, N., Ryu, M., Sakai, D., Chung, H., Kawakami, H., Yabusaki, H., Lee, J., Saito, K., Kawaguchi, Y., Kamio, T., Kojima, A., Sugihara, M., & Yamaguchi, K. (2020). Trastuzumab deruxtecan in previously treated HER2-Positive gastric cancer. New England Journal of Medicine/the New England Journal of Medicine, 382(25), 2419–2430. https://doi.org/10.1056/nejmoa2004413

Vis, M. a. M., Ito, K., & Hofmann, S. (2020). Impact of Culture Medium on Cellular Interactions in in vitro Co-culture Systems. Frontiers in Bioengineering and Biotechnology, 8. https://doi.org/10.3389/fbioe.2020.00911
