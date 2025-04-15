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


