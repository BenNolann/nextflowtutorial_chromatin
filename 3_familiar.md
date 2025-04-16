---
layout: default
title: Familiar
---

## Basic Structure of Nextflow

Channels

Operators

Processes

## Our First Script

For our first look into Nextflow, we will be using a simple script that counts the number of words in a fastq.

1. Copy the script to our work directory.

    ```bash
    cp scripts/introduction/word_count.nf .
    ```

    Have a look inside

    ```bash
    more word_count.nf
    ```

2. Run the script!

    ```bash
    nextflow run word_count.nf
    ```

3. Change a parameter

    ```bash
    nextflow run word_count.nf --input 'data/yeast/reads/ref2_*.fq.gz'
    ```

4. Parameter changes as an input file instead

    Copy this JSON file that has updated parameters for word_count.nf

    ```bash
    cp scripts/parameters/wc-params.json .
    more wc-params.json
    ```

    Run this pipeline again but with the JSON file

    ```bash
    nextflow run word_count.nf -params-file wc-params.json
    ```

**NOTE**: 

* Parameters for Nextflow are used with `-`
* Parameters for your Nextflow script are used with `--`

