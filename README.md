# Variant Calling Workflow Demo

- Understanding the steps involved in variant calling.
- Describing the types of data formats encountered during variant calling (FASTQ, SAM/BAM, VCF)
- Using command line tools to perform variant calling. Run [variant_calling_workflow.ipynb](https://github.com/roshni-b/variant-calling/blob/main/variant_calling_workflow.ipynb) for a [bcftools](https://samtools.github.io/bcftools/bcftools.html) demo.

### Variant Calling

A variant call is a conclusion that there is a nucleotide difference vs. some reference at a given position in an individual genome or transcriptome, often referred to as a Single Nucleotide Polymorphism (SNP). The call is usually accompanied by an estimate of variant frequency and some measure of confidence.

### Environment set-up

```
conda env create -f environment.yml
conda activate vc-env
```

### Final Directory structure

```
.
├── data
│   ├── ref_genome
│   │   ├── ecoli_rel606.fasta
│   │   ├── ecoli_rel606.fasta.amb
│   │   ├── ecoli_rel606.fasta.ann
│   │   ├── ecoli_rel606.fasta.bwt
│   │   ├── ecoli_rel606.fasta.fai
│   │   ├── ecoli_rel606.fasta.pac
│   │   └── ecoli_rel606.fasta.sa
│   └── trimmed_fastq_small
│       ├── SRR2584863_1.trim.sub.fastq
│       ├── SRR2584863_2.trim.sub.fastq
│       ├── SRR2584866_1.trim.sub.fastq
│       ├── SRR2584866_2.trim.sub.fastq
│       ├── SRR2589044_1.trim.sub.fastq
│       └── SRR2589044_2.trim.sub.fastq
├── environment.yml
├── results
│   ├── bam
│   │   ├── SRR2584866.aligned.bam
│   │   ├── SRR2584866.aligned.sorted.bam
│   │   └── SRR2584866.aligned.sorted.bam.bai
│   ├── bcf
│   │   ├── SRR2584866_raw.bcf
│   │   └── SRR2584866_variants.vcf
│   ├── sam
│   │   └── SRR2584866.aligned.sam
│   └── vcf
│       └── SRR2584866_final_variants.vcf
├── sub.tar.gz
└── variant_calling_workflow.ipynb
```