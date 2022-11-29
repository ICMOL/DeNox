## Introduction

Liquid chromatography coupled with tandem mass spectrometry (LC-MS/MS) has become a conventional platform for exploring the mystery of cellular activities. The acquired MS data are often processed by available software tools for molecular identification and quantitation. Quality control is an essential step to ensure the accurate molecular measurement because contaminants or mechanical artifacts inevitably exist in the acquired MS data. Data visualization is the most straightforward solution for quality control, in which users can directly access raw files to inspect the quality of signals and the level of noises. Here we present a software tool, called DeNox, which can efficiently extract signals of interest from LC-MS data (given protein database search reports or quantified metabolites) and export them in three different dimensions, including (1) m/z and retention time, (2) m/z and intensity, and (3) retention time and intensity. DeNox can process multiple raw files simultaneously and is suitable for proteomic and metabolomic researches.

## How to Use

### Input Files
* A report file, e.g., a PSM table from FragPipe or a metabolite quantitation file from iMet-Q or XCMS
* Raw data in **mzML file format**

### System Requirement

- [Java SE Runtime Environment 11(or above)](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html) is required to be installed prior to use DeNox. 


### Step 1. Choose the source of LC-MS data

<img src="https://github.com/ICMOL/DeNox/blob/main/source.png">

### Step 2. Load the input files

- Report file parameter

  DeNox needs two parameters (m/z and retention time) to extract signals from LC-MS data. For metabolomics, the two parameters must be named as **mass_to_charge** and **retention_time**. For proteomics, they must be named as **Observed M/Z** and **Retention**. Please note that the unit of retention time is minute.

<img src="https://github.com/ICMOL/DeNox/blob/main/input.png">

- Advanced options

|        Name         |  Default Value | Comments |
|---------------------|----------------|------------------------------|
| RT tolerance(min.)  | 0.5            | the tolerance of retention time (unit: minutes) |
| Image filter        | black          | heatmap background color |

<img src="https://github.com/ICMOL/DeNox/blob/main/options.png">

### Step 3. Display the figures
One can double click a row (for proteomic PSM tables) or a cell (for metabolomic reports) to display the figures.



