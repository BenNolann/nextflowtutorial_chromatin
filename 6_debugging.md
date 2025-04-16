---
layout: default
title: Debugging
---

## How to debug Nextflow

When you run a nextflow pipeline, a bunch of data is saved about that run and it is all saved in your directory. But there's a lot of files and it can be quite overwhelming. The key is to understand what to look for and then you can really take advantage of all this information. 

1. What recent pipeline runs have I done?

    ```bash
    nextflow log
    ```

    Too many? Shorten the output

    ```bash
    nextflow log | tail
    ``` 

2. My pipeline gave a weird result/ or it failed! How do I investigate this?

    We need to look inside the log file for our nextflow run. The most recent is saved as `.nextflow.log`, the second last is saved as `.nextflow.log.1` up to `.nextflow.log.9`. After 10 pipeline runs you'll start losing these log files unless you're saving them somewhere.

    ```bash
    tail .nextflow.log
    ```

    For every event that saw data go through a process in your pipeline, you'll find an entry in this log. It will look something like this:

    ```
    Apr-16 15:05:47.471 [Task submitter] INFO  nextflow.Session - [9e/7963cf] Submitted process > NUMLINES (6)
    ```
    **NOTE:** the [9e/7963cf]. This is unique to this event. Yours will be different.

    This is where you can investigate that event. 

    In Nextflow, you will notice a `work` directory saved where you've been running these pipelines. All of these 'events' are stored here. The power of Nextflow is in here, despite it looking terrifying.