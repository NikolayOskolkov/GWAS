![](images/logo.png)

# Genome-Wide Association Studies (GWAS) for Evolutionary Biology

## Instructor

- Dr. Nikolay Oskolkov, Group Leader (PI) at NIRI, Riga, Latvia

## Course overview

Genome-Wide Association Studies (GWAS) have become a cornerstone of modern genetics, enabling researchers to identify genetic variants associated with complex traits, disease, adaptation, and evolutionary processes. Large-scale genotyping and sequencing projects now make it possible to investigate the genetic architecture of phenotypic variation across populations and species. This course provides a practical introduction to GWAS methodology, from data generation and quality control through association testing, meta-analysis, and polygenic prediction.

Participants will learn how to process and analyze genome-wide genotype data, run association studies with widely used software (PLINK, SNPTEST, GWAMA, METAL), visualize and interpret the results, and build polygenic risk scores. The course also covers modern genomic data processing with GATK, population structure correction, and the open problem of missing heritability. Through worked examples on real datasets, you will gain the skills to design, run, and critically evaluate GWAS analyses in evolutionary biology and related fields.

## Target audience and assumed background

The course is intended for evolutionary biologists, population geneticists, bioinformaticians, medical geneticists, quantitative biologists, postgraduate students, and early-career researchers interested in GWAS and complex trait genetics. We assume a basic understanding of genetics, molecular biology, and statistics, and some familiarity with the command line and R. Prior experience with genomic datasets, population genetics, or NGS data is helpful but not required.

## Learning outcomes

By completing this course, you will:

- Understand the principles of genetic variation and genome-wide association studies
- Know the goals and contributions of major reference resources: HapMap, 1000 Genomes, HGDP, and ERGA
- Be able to phase and impute genotype data with PHASEIT2 and IMPUTE2
- Apply best-practice genotype QC: Hardy-Weinberg equilibrium, SNP call rate, and minor allele frequency/count filters
- Perform association testing with PLINK and SNPTEST, and meta-analysis with GWAMA and METAL
- Process NGS data with GATK best practices, from alignment and base quality recalibration to variant calling with HaplotypeCaller
- Carry out permutation testing and conditional association analyses, and parallelize large GWAS computations
- Visualize results with Manhattan plots and LocusZoom, and correct for population structure using PCA
- Construct and validate polygenic risk scores on independent datasets
- Understand the missing heritability problem and current approaches to addressing it 

---

# Schedule

## Before the course

| Time   | Activity                                                                                           |Link                                                                                                            |
|--------|----------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| ~ 1 h  | Recorded talk: AaRCademy workshop: aDNA data processing with Nikolay Oskolkov                      | [Video](https://www.youtube.com/watch?v=-nWoq6NTBd0&t=2121s)                                                                                           |
| ~ 2 h  | DNAHarvester: a pipeline for analysis of highly degraded DNA from low-covarege samples             | [PDF](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/articles/2026.04.20.719564v2.full.pdf)                                                                                 |
| ~ 1 h  | Useful reading: how the curse of dimensionality complicates genomics analysis                      | [Blog](https://medium.com/data-science/genomics-new-clothes-6301ab9798a7?sk=db5db53c7f968add8a4b9a82579bf56d)                                                                          |
| ~ 1 h  | In case needed: Recap on basic Unix commands                                                       | [Lab](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/command-line-basics.md)                                                                                                    |


## Day 1: 3 pm - 9 pm Swedish time

| Time           | Activity                                                                                   |Link                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 15.00 - 15.30  | Course outline and practical information, introductions of participants                    | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day1/course_outline.pdf)                                                                                           |
| 15.30 - 16.30  | Challenges of high-dimensional genomics data analysis                                      | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day1/ChallengesGenomics.pdf)                                                                                       |
| 16.30 - 17.30  | Introduction to Next Generation Sequencing (NGS) data, BWA alignment and GATK workflow     | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day1/NGS_workflow_GATK.pdf)                                                                                        |
| 17.30 - 18.30  | Break                                                                                      |                                                                                                                |
| 18.30 - 19.00  | Probabilistic variant calling from low-coverage genomics data with ANGSD                   | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day1/ANGSD.pdf)                                                                                                    |
| 19.00 - 20.30  | Practical: quality control, adapter removal and alignment with BWA MEM                     | [Lab](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day1/QC_Alignment_Colab.ipynb)                                                                                     |
| 19.00 - 20.30  | Practical: variant calling from low-coverage genomics data with ANGSD                      | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day1/ANGSD_Lab_GoogleColab.html)                                                                   |
| 20.30 - 21.00  | Questions and discussion                                                                   |



## Day 2: 3 pm - 9 pm Swedish time

| Time           | Activity                                                                                   |Link                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 15.00 - 16.00  | Bonus material: introduction to imputation and genetic imputation with IMPUTE2             | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day2/imputation.pdf)                                                                                               |
| 15.00 - 16.00  | Principal Components Analysis (PCA) for population genomics applications                   | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day2/PCA_PopGen.pdf)                                                                                               |
| 16.00 - 17.30  | Nonlinear dimensionality reduction with tSNE and UMAP for population genomics applications | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day2/DimReduct_PopGen.pdf)                                                                                         |
| 17.30 - 18.30  | Break                                                                                      |                                                                                                                |
| 18.30 - 19.30  | Practical: coding PCA and Multi-Dimensional Scaling (MDS) from scratch                     | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day2/pca_mds_toy_example.html)                                                                     |
| 18.30 - 19.30  | Practical: practicing PCA, MDS, tSNE and UMAP                                              | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day2/Dimension_Reduction_tutorial.html)                                                            |
| 19.30 - 20.30  | Practical: horseshoue effect in PCA, coding from scratch and exploring block structure     | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day2/WhyPCALooksTriangular.html)                                                                   |
| 20.30 - 21.00  | Questions and discussion                                                                   |



## Day 3: 3 pm - 9 pm Swedish time

| Time           | Activity                                                                                   |Link                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 15.00 - 16.00  | Introduction to clustering algorithms: hierarchical and partition clustering               | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day3/IntroClustering.pdf)                                                                                          |
| 16.00 - 17.30  | Admixture analysis and admixture inference from low-coverage data with NGSadmix            | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day3/Admixture.pdf)                                                                                                |
| 17.30 - 18.30  | Break                                                                                      |                                                                                                                |
| 18.30 - 19.30  | Practical: admixture inference from low-coverage data with NGSadmix                        | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day1/ANGSD_Lab_GoogleColab.html)                                                                   |
| 19.30 - 20.30  | Practical: maximum likelihood admixture inference with Admixture tool                      | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day3/ADMIXTURE_Colab.html)                                                                         |
| 19.30 - 20.30  | Practical: practicing hierarchical, partitioning and density-based clustering              | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day3/Clustering_Lab.html)                                                                          |
| 19.30 - 20.30  | Practical: practicing Gaussian Mixture Model (GMM) underlying STRUCTURE software           | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day3/GMM_FromScratch.html)                                                                         |
| 20.30 - 21.00  | Questions and discussion                                                                   |


## Day 4: 3 pm - 9 pm Swedish time

| Time           | Activity                                                                                   |Link                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 15.00 - 16.00  | Phylogenetic analysis: genetic and evolutionary distance, phylogenetic tree construction   | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day3/PhylogeneticAnalysis.pdf)                                                                                     |
| 16.00 - 16.30  | Introduction to selection and drift of allele frequencies: Wright-Fisher model             | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day4/selection.pdf)                                                                                                |
| 16.30 - 17.30  | Practical: practicing natural selection vs genetic drift Wright-Fisher model               | [Lab](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day4/Selection_vs_Drift.ipynb)                                                                                     |
| 17.30 - 18.30  | Break                                                                                      |                                                                                                                |
| 18.30 - 19.30  | Nucleotide diversity, population differentiation, Tajima's D and Fst selection analyses    | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day4/F_statistics.pdf)                                                                                             |
| 19.30 - 20.30  | Practical: computation of Fst from low-coverage data within ANGSD workflow                 | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day4/Fst_Colab.html)                                                                               |
| 19.30 - 20.30  | Practical: computation of F2 statistics and clustering using AADR dataset                  | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day4/F2_statistics_AADR_heatmap.html)                                                              |
| 20.30 - 21.00  | Questions and discussion                                                                   |


## Day 5: 3 pm - 9 pm Swedish time

| Time           | Activity                                                                                   |Link                                                                                                            |
|----------------|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 15.00 - 16.00  | Practical: computation of F3 statistics for an Unknown population in AADR dataset          | [Lab](https://html-preview.github.io/?url=https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day5/F3_outgroup_AADR.html)                                                                        |
| 16.00 - 17.30  | Introgression analysis with D-statistic and applications to ancient DNA                    | [Slides](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/slides/Day5/Dstat.pdf)                                                                                                    |
| 17.30 - 18.30  | Break                                                                                      |                                                                                                                |
| 18.30 - 19.30  | Practical: computation of D-statistic on Nenderthal and modern human genomics data         | [Lab](https://github.com/NikolayOskolkov/PopGen_PopStructure/blob/main/practicals/Day5/Dstat_ABBA_BABA_Colab.ipynb)                                                                                  |
| 19.30 - 20.30  | Practical: D-statistic, F4 and F4-ratio computations via admixR software                   | [Lab](https://bodkan.net/admixr/articles/vignette-01-tutorial.html)                                                                                  |
| 20.30 - 21.00  | Questions and discussion                                                                   |

