---
layout: default
title: Slingshot
---

## Let's look at a very simple RNA-seq pipeline.

We're now going to run a script that performs the following steps:

1. Create a salmon Index
2. Perform transcript quantification using Salmon
    **NOTE:** We don't align to the genome here because Salmon is an alignment-free transcript quantification tool.
3. Run FASTQC on our fastq reads
4. Perform MULTIQC which aggregates our metric data into a single html document for us to look at.

    ```bash
    cp scripts/rnaseq_pipeline/script7.nf .
    ```

You can use this script as a template to develop a pipeline that is as complicated or as simple as you would like.

There are many levels to this, a very complicated Nextflow pipeline can be seen here: [nf-core](https://github.com/nf-core/chipseq)

A much less complex version that I wrote myself is here: [jrowleylab](https://github.com/JRowleyLab/chipseq-nf)

Both are useful, and it's up to you whether you want full control over the pipeline or not. ie. use existing pipelines or write your own.