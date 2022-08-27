## Introduction
The acquired MS data are often processed by available software tools for molecular identification and quantitation. Quality control is an essential step to ensure the accurate molecular measurement because contaminants or mechanical artifacts inevitably exist in the acquired MS data. Here we present a software tool, called DeNox, which can efficiently extract signals of interest from LC-MS data (given protein database search reports or quantified metabolites). DeNox can process multiple raw files simultaneously and is suitable for proteomic and metabolomic researches.

## How to Use

To extract signals of interest from LC-MS data, DeNox requires report file (In metabolomic, e.g., i-MetQ, XCMS) or an identification result (In proteomic, e.g., MSFragger) as input file.

### System Requirement

### Step 1. Choose source for LC-MS data

<img src="https://github.com/ICMOL/DeNox/blob/main/source.png">

### Step 2. Load input file

LC-MS data must be in mzML format.

- Report file parameter

  Report file has two parameter: m/z and retention time: In **metabolomic**, they must name as **mass_to_charge** and **retention_time** respectively. In **proteomic**, they must name as **Retention** and **Observed M/Z** respectively.

<img src="https://github.com/ICMOL/DeNox/blob/main/input.png">

- Advanced options

|        Name         |  Default Value | Comments |
|---------------------|----------------|------------------------------|
| RT tolerance(min.)  | 0.5            | the tolerance of retention time (unit: minutes) |
| M/Z tolerance(ppm)  | 0.03           | the tolerance of mass to charge (unit: ppm) |
| Image filter        | black          | heatmap background color |

<img src="https://github.com/ICMOL/DeNox/blob/main/options.png">


### Step 3. Extract signals

In the report table of metabolomic, to double click the quantity value under the sample name.

In the report table of proteomic, to double click the spectrum data of interest.

