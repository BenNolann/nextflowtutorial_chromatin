---
layout: default
title: Asynchronous
---

## How Nextflow Works

Nextflow runs each input sample in an asynchronous nature.

![alt text](async.png)


1. Run the following script

    ```bash
    nextflow run scripts/process/process_input_value.nf -process.debug
    ```

2. Explain what the script is doing.

3. Rerun the script. Has anything changed?

## Counting lines in multiple files

1. Run the following script

    ```bash
    nextflow run scripts/process/process_input_file.nf -process.debug
    ```
2. Rerun the script again. 