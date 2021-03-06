# G2Vec-AMR-Embeddings

## Summary
Application of deep learning methodology G2Vec [1] to gene neighborhood genome data for the analysis of antimicrobial resistance (AMR) conferring genes and evaluation of Resistance Gene Identifier (RGI) [2] Loose Hits using models trained on Perfect and Strict hits. 

## Background
The analysis of gene neighborhoods is highly applicable to the task of understanding and identifying the presence of antimicrobial resistance (AMR) genes in bacterial genomes. In prokaryotic genomes, co-regulated genes that are proximal on the same operon (a cluster of genes controlled by the same operator) typically share functionality and may share evolutionary histories [3]. Because of this, it may be possible to infer functionality, history, or other information for an unrecognized gene if the functions and properties of its neighboring genes are known, and vice versa. Utilizing genomic context information can therefore significantly downsize the ‘search space’ of computational studies and increase the likelihood of predicting interactions and functionalities that are verifiable in vitro [3].

Generating feature representations or embeddings for genomic data has arisen as a promising means of preserving gene context information.  While traditionally applied to words in natural language processing to map words to vectors in a way that preserves their semantics and can lead to the discovery of interesting associations, gene embeddings have been used to make biological relevance predictions using machine learning models with high performance [1, 4]. Additionally, networks are another representation method that can be applied to genomic data in order to preserve gene context information. In gene networks, each node represents a gene, and edges between two nodes represent an existing relationship between genes, the latter of which typically corresponds to either functional interaction, co-expression, or some measure of physical proximity [1, 4].

One method that combines gene embeddings with network based learning is G2Vec, a deep learning method introduced by Choi et al. capable of identifying gene signatures through distributed gene representations [1]. It was implemented for the purpose of predicting cancer prognostic genes [1], but has relevance for AMR prediction tasks as G2Vec offers a practical methodology for preserving gene context information.

This project seeks to apply G2Vec to the analysis and identification of candidate AMR-conferring genes It also focuses on the visual analysis of gene neighborhoods of AMR genes.

## Workflow

<p align="center">
  <img src="https://github.com/JTL-lab/G2Vec-AMR-Embeddings/blob/main/assets/workflow-visualization.png" alt="Workflow diagram for embedding generation, model training, and use" width=50% height=50%>
</p>

## Acknowledgement

### Input data files

Genome data was obtained from NCBI.

Prokka [5], Roary [6], and RGI [2] were used for data preprocessing.

### G2Vec 
This project utilizes source code from G2Vec [1], created by Choi et al. for the purpose of identifying biomarkers for cancer prognosis. Code was migrated to Tensorflow 2.0.

Link to repository: https://github.com/mathcom/G2Vec

## References

[1] Choi J, Oh I, Seo S, Ahn J. G2Vec: Distributed gene representations for identification of cancer prognostic genes. Sci Rep. 2018 Sep 13;8(1):13729. doi: 10.1038/s41598-018-32180-0. PMID: 30213980; PMCID: PMC6137174.

[2] Alcock, B. P., Raphenya, A. R., Lau, T. T. Y., Tsang, K. K., Bouchard, M., Edalatmand, A., Huynh, W., Nguyen, A. V., Cheng, A. A., Liu, S., Min, S. Y., Miroshnichenko, A., Tran, H., Werfalli, R. E., Nasir, J. A., Oloni, M., Speicher, D. J., Florescu, A., Singh, B., Faltyn, M., Hernandez, K. A., Sharma, A. N., Bordeleau, E., Pawlowski, A. C., Zubyk, H. L., Dooley, D., Griffiths, E., Maguire, F., Winsor, G. L., Beiko, R. G., Brinkman, F. S. L., Hsiao, W. W. L., Domselaar, G. V., and McArthur, A. G. (2020). CARD 2020: antibiotic resistome surveillance with the comprehensive antibiotic resistance database (Version 5.2.0) [Computer software]. https://doi.org/10.1093/nar/gkz935

[3] Aravind, L. (2000). Guilt by association: Contextual information in genome analysis. \emph{Genome Research}, 10(8), 1074–1077. DOI: 10.1101/gr.10.8.1074

[4] Du, J., Jia, P., Dai, Y., Tao, C., Zhao, Z., and Zhi, D. (2019). Gene2vec: Distributed representation of genes based on co-expression. \emph{BMC Genomics}, 20(Suppl 1). DOI: 10.1186/s12864-018-5370-x

[5] Seemann T. Prokka: rapid prokaryotic genome annotation. Bioinformatics. 2014 Jul 15;30(14):2068-9. doi: 10.1093/bioinformatics/btu153. Epub 2014 Mar 18. PMID: 24642063.

[6] Andrew J. Page, Carla A. Cummins, Martin Hunt, Vanessa K. Wong, Sandra Reuter, Matthew T. G. Holden, Maria Fookes, Daniel Falush, Jacqueline A. Keane, Julian Parkhill, "Roary: Rapid large-scale prokaryote pan genome analysis", Bioinformatics, 2015;31(22):3691-3693 doi:10.1093/bioinformatics/btv421


