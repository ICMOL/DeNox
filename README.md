## Introduction

<div align=center><img width="350" height="200" src="https://github.com/ICMOL/DeNox/blob/main/images/home.PNG"><div>

<div align=left> 
Liquid chromatography coupled with tandem mass spectrometry (LC-MS/MS) has become a conventional platform for exploring the mystery of cellular activities. The acquired MS data are often processed by available software tools for molecular identification and quantitation. Quality control is an essential step to ensure the accurate molecular measurement because contaminants or mechanical artifacts inevitably exist in the acquired MS data. Data visualization is the most straightforward solution for quality control, in which users can directly access raw files to inspect the quality of signals and the level of noises. Here we present a software tool, called DeNox, which can efficiently extract signals of interest from LC-MS data (given protein database search reports or quantified metabolites) and export them in three different dimensions, including (1) m/z and retention time, (2) m/z and intensity, and (3) retention time and intensity. DeNox can process multiple raw files simultaneously and is suitable for proteomic and metabolomic researches.

## How to Use

### System Requirement

- [Java SE Development Kit 11(or above)](https://www.oracle.com/tw/java/technologies/javase/jdk11-archive-downloads.html) is required to be installed prior to use DeNox. 


### Step 1. Set parameter and choose


|        Name         |  Default Value | Comments |
|---------------------|----------------|------------------------------|
| Source              | proteomics or metabolomics | the analytical sources for proteomics/metabolomics |
| TIme Unit           | min. or sec.   | the time unit of report file |
| m/z Column Name     | user-defind    | mass-to-charge of column name in report file |
| RT Column Name      | user-defind    | retention time of column name in report file |
| RT tolerance(min.)  | 0.5            | the tolerance of retention time (unit: minutes) |
| lower m/z (Da)      | 1              | the lower limit of the mass-to-charge ratio (unit: dalton) |
| upper m/z (Da)      | 3              | the upper limit of the mass-to-charge ratio (unit: dalton) |

### Step 2. Input Files

* A feature table, e.g., a PSM table from FragPipe or a metabolite quantitation file from iMet-Q or XCMS in **csv/tsv file format**
* Raw data in **mzML file format**

![image](https://github.com/ICMOL/DeNox/blob/main/images/input.PNG)
 

### Step 3. Display figures

#### Raw data visualization

Elution heatmap: m/z vs. retention time

Extracted ion chromatogram: retention time vs. intensity

Spectrum Information: m/z vs. intensity

#### Peak Quality Assessments

These measures are used to quantify the overall peak shape and retention time consistency between samples.
 
![image](https://github.com/ICMOL/DeNox/blob/main/images/output.PNG)

https://github.com/ICMOL/DeNox/assets/86774336/0aff22f3-b249-4cfc-9754-21a90176b69d



