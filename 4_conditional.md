---
layout: default
title: Conditional
---

## Conditional Parameters

You can tell the pipeline which path to take for your analysis. You can have multiple options for tools to use and let the user decide which one to go with.

1. Copy over a new script, this one is similar to the word_count but has an `if()` statement in there.

    ```bash
    cp scripts/process/process_conditional.nf

    more process_conditional.nf
    ```

2. Run the script with the `-process.debug` parameter to print out the `echo` statements. 

    ```bash
    nextflow run process_conditional.nf -process.debug
    ```
3. Change the parameter 'method' to alter the path the script takes.

    ```bash
    nextflow run process_conditional.nf -process.debug --method 'bases'
    ```
