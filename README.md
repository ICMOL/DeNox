## Introduction

Liquid chromatography coupled with tandem mass spectrometry (LC-MS/MS) has become a conventional platform for exploring the mystery of cellular activities. The acquired MS data are often processed by available software tools for molecular identification and quantitation. Quality control is an essential step to ensure the accurate molecular measurement because contaminants or mechanical artifacts inevitably exist in the acquired MS data. Data visualization is the most straightforward solution for quality control, in which users can directly access raw files to inspect the quality of signals and the level of noises. Here we present a software tool, called DeNox, which can efficiently extract signals of interest from LC-MS data (given protein database search reports or quantified metabolites) and export them in three different dimensions, including (1) m/z and retention time, (2) m/z and intensity, and (3) retention time and intensity. DeNox can process multiple raw files simultaneously and is suitable for proteomic and metabolomic researches.

## How to Use

### Input Files
* A report file, e.g., a PSM table from FragPipe or a metabolite quantitation file from iMet-Q or XCMS
* Raw data in mzML file format

### System Requirement

是否需要安裝 JRE?


### Step 1. Choose source for LC-MS data

<img src="https://github.com/ICMOL/DeNox/blob/main/source.png">

### Step 2. Load input file

LC-MS data must be in mzML format.

- Report file parameter

  Report file has two parameter: m/z and retention time: In **metabolomic**, they must name as **mass_to_charge** and **retention_time** respectively. In **proteomic**, they must name as **Observed M/Z** and **Retention** respectively.

<img src="https://github.com/ICMOL/DeNox/blob/main/input.png">

- Advanced options

|        Name         |  Default Value | Comments |
|---------------------|----------------|------------------------------|
| RT tolerance(min.)  | 0.5            | the tolerance of retention time (unit: minutes) |
| M/Z tolerance(ppm)  | 0.03           | the tolerance of mass to charge (unit: ppm) |
| Image filter        | black          | heatmap background color |

<img src="https://github.com/ICMOL/DeNox/blob/main/options.png">


### Step 3. Extract signals

Double click the quantity value under the sample name from metabolomic report table.

Double click the spectrum data of interest from proteomic report table.

