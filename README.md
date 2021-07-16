# TE_expression_BLCA
Repo  for transposon-element expression in bladder cancer samples in TCGA (TCGA-BLCA).

For gene expression analysis , the method explained in Yu Kong et al. [(Nature Communications volume 10, Article number: 5228 (2019))](https://www.nature.com/articles/s41467-019-13035-2), which they called REdiscoverTE was used. More details on how this tools works can be find [here](http://research-pub.gene.com/REdiscoverTEpaper/software/REdiscoverTE_README.html).

Diffrent kind of expression data were generated for 433 TCGA-BLCA cases and here is short description on each files(adapted from the software manual):

GENE: Transcript-level expression values:

- GENE_1_raw_counts.RDS: raw counts DGEList data object.
- GENE_2_counts_normalized.RDS: normalized counts (by total gene counts) DGEList data object.
- GENE_3_TPM.RDS: TPM (transcripts per million) for each gene/transcript. DGEList data object.

Repetitive elements

- RE all: Repetitive elements found anywhere in the genome. Granularity for all RE reporting is at repName level (where the three levels we use are name, family, and class, in increasing order of generality).
  - RE_all_1_raw_counts.RDS: raw counts DGEList data object.
  - RE_all_2_counts_normalized.RDS: note that counts are normalized by total gene counts
  - RE_all_3_TPM.RDS: TPM (transcripts per million) for each repetitive element ‘repName’. DGEList data object.

- RE exon: Subset of RE all: only repetitive elements found at least partially within an annotated exon.
  - RE_exon_1_raw_counts.RDS: raw counts DGEList data object.
  - RE_exon_2_counts_normalized.RDS: counts are normalized by total gene counts
   - RE_exon_3_TPM.RDS: TPM (transcripts per million) for each repetitive element ‘repName’. DGEList data object.
   - 
- RE intron: Subset of RE all: only repetitive elements that do not have any overlap with an exon, and have some overlap with an intron.
  - RE_intron_1_raw_counts.RDS: raw counts DGEList data object.
  - RE_intron_2_counts_normalized.RDS:counts are normalized by total gene counts
  - RE_intron_3_TPM.RDS: TPM (transcripts per million) for each repetitive element ‘repName’. DGEList data object.
  - 
- RE intergenic: Subset of RE all: only repetitive elements that have no overlap with annotated introns or exons.
  - RE_intergenic_1_raw_counts.RDS: raw counts DGEList data object.
  - RE_intergenic_2_counts_normalized.RDS: counts are normalized by total gene counts
  - RE_intergenic_3_TPM.RDS: TPM (transcripts per million) for each repetitive element ‘repName’. DGEList data object.
