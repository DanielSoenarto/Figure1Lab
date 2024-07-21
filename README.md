# cancer-cell-lines-scRNA-seq-data-exploration

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

## References
Gajria, D., & Chandarlapaty, S. (2011). HER2-amplified breast cancer: mechanisms of trastuzumab resistance and novel targeted therapies. Expert Review of Anticancer Therapy, 11(2), 263–275. https://doi.org/10.1586/era.10.226

Haque, A., Engel, J., Teichmann, S. A., & Lönnberg, T. (2017). A practical guide to single-cell RNA-sequencing for biomedical research and clinical applications. Genome Medicine, 9(1). https://doi.org/10.1186/s13073-017-0467-4

Jovic, D., Liang, X., Zeng, H., Lin, L., Xu, F., & Luo, Y. (2022). Single‐cell RNA sequencing technologies and applications: A brief overview. Clinical and Translational Medicine, 12(3). https://doi.org/10.1002/ctm2.694

Kazazi-Hyseni, F., Beijnen, J. H., & Schellens, J. H. (2010). Bevacizumab. The oncologist, 15(8), 819–825. https://doi.org/10.1634/theoncologist.2009-0317
Mirabelli, P., Coppola, L., & Salvatore, M. (2019). Cancer Cell Lines Are Useful Model Systems for Medical Research. Cancers, 11(8), 1098. https://doi.org/10.3390/cancers11081098

Shitara, K., Bang, Y., Iwasa, S., Sugimoto, N., Ryu, M., Sakai, D., Chung, H., Kawakami, H., Yabusaki, H., Lee, J., Saito, K., Kawaguchi, Y., Kamio, T., Kojima, A., Sugihara, M., & Yamaguchi, K. (2020). Trastuzumab deruxtecan in previously treated HER2-Positive gastric cancer. New England Journal of Medicine/the New England Journal of Medicine, 382(25), 2419–2430. https://doi.org/10.1056/nejmoa2004413
