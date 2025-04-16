---
layout: default
title: Build
---

First we need to get our Software in order.

## SLURM

1. Allocate memory for this session

    ```bash
    srun --qos=short --mem=5gb --time=03:00:00 --pty $SHELL
    ```

1. Load miniforge and nano modules

    ```bash
    module purge
    module load miniforge nano
    ```

## Setting up a Conda environment

1. Download the yaml file: 

    ```bash
    wget https://raw.githubusercontent.com/BenNolann/nextflowtutorial_chromatin/refs/heads/main/environment_hcc.yml
    ```

    (OPTIONAL) Look inside with:

    ```bash
    nano environment_hcc.yml
    ```

1.  Build conda environment (mamba is the same thing it's just written in C++ and is faster.)

    ```bash
    mamba env create -n nf-training -f environment_hcc.yml
    ```

1. Activate environment

    ```bash
    conda activate nf-training
    ```

## Getting Test Data and Test Nextflow Scripts

Downloading our test data and pre-made short Nextflow scripts for you to experiment with and tweak.

1. Download a bunch of test data. Heavily subsampled fastq files that will run very fast.

    ```bash
    wget --content-disposition https://ndownloader.figshare.com/files/28531743
    ```
    
2. Decompress the data and remove the compressed version.
    
    ```bash
    tar -xvf data.tar.gz
    rm data.tar.gz
    ```

3. Download test repository

    ```bash
    wget https://github.com//carpentries-incubator/workflows-nextflow/archive/main.zip
    ```

4. Decompress zip, remove zip, grab scripts from repo, and delete the repo.

    ```bash
    unzip main.zip
    rm main.zip
    mv workflows-nextflow-main/episodes/files/scripts/ .
    rm -rf workflows-nextflow-main/
    ```