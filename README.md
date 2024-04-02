# Pig-annotation

the genome fasta file was downloaded from NCBI:
https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_000003025.6/

All nucleotides were converted to upper case:
GCF_000003025.6_Sscrofa11.1_genomic.upper.fasta

Repeat families were identified using repeat modeler:
repeats.out, repeats_stats.txt

Repeat families were used to mask the repeats in the genome (convert repeat regions to lower case):
GCF_000003025.6_Sscrofa11.1_genomic.upper.masked.fasta

braker2 was used to annotate the masked genome fasta file, braker2 needs two inputs: 1-masked genome fasta file, 2- protein database to generate hints.
We used the metazoa orthodb database dowloaded from: https://bioinf.uni-greifswald.de/bioinf/partitioned_odb11/Metazoa.fa.gz
braker2 output gtf file:pig.braker.gtf


Helixer was also used to annotated the genome fasta file:
Helixer output gtf file:pig.helixer.gtf

predicted proteins were extracted and functionally annotated with interproscan and pannzer, output files were merged and converted to tabular format:
braker_functional_annotation.tsv
helixer_functional_annotation.tsv
