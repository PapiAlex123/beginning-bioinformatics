# NASA RR-1 Sample-Size Benchmark

## Project Overview

This project investigates how reliably differential-expression (DE) analysis methods identify gene expression changes in mouse soleus muscle during spaceflight, and how the results change when the number of biological replicates is reduced.

The project uses RNA-seq data from NASA's Rodent Research-1 (RR-1) mission. It compares Space Flight samples with Ground Control samples and examines the stability of differential-expression results at smaller sample sizes.

## Research Question

How reliably do differential-expression methods recover spaceflight-associated gene expression changes as the number of biological replicates decreases, and how well do different methods agree?

## Dataset

- **Source:** NASA Open Science Data Repository (OSDR)
- **Study:** OSD-104 / GLDS-104
- **Experiment:** Rodent Research-1 (RR-1)
- **Tissue:** Mouse soleus muscle
- **Organism:** Mouse (*Mus musculus*)
- **Samples:** 12 total
- **Groups:** 6 Space Flight and 6 Ground Control
- **Data type:** Bulk RNA-seq gene count data

Dataset link: https://osdr.nasa.gov/bio/repo/data/studies/OSD-104

## Methods and Tools

The project uses Python in Google Colab for data processing and analysis.

Methods include:

- Data validation and sample quality control
- Exploratory Principal Component Analysis (PCA)
- Differential-expression analysis using PyDESeq2
- Preliminary comparison with an InMoose edgeR-style analysis
- Sample-size reduction and stability benchmarking (planned)
- Comparison of differential-expression methods (planned)
- Welch t-test baseline (planned)

## Repository Contents

```text
project/
├── README.md
├── NASA_RR1_Sample_Size_Benchmark.ipynb
├── ai_usage.md
```

- **README.md:** Project overview, dataset, methods, and repository guide.
- **NASA_RR1_Sample_Size_Benchmark.ipynb:** Main notebook containing the analysis.
- **ai_usage.md:** Documentation of AI tools used during the project.
- **environment.yml:** Software environment and package information.
- **figures/:** Figures generated during the analysis.

## Current Progress

### Completed

- Downloaded and examined the NASA RR-1 RNA-seq dataset.
- Validated the count matrix and aligned samples with metadata.
- Performed sample quality control.
- Performed exploratory PCA.
- Completed preliminary full-data differential-expression analysis using PyDESeq2.
- Performed a preliminary InMoose edgeR-style analysis.

### In Progress / Planned

- Improve and validate the edgeR-style analysis.
- Perform sample-size reduction experiments.
- Compare differential-expression results across methods and sample sizes.
- Add a Welch t-test baseline.
- Perform a sensitivity analysis using RSEM counts.
- Complete the benchmark metrics and final figures.

## How to Use

The analysis notebook is designed to be run in Google Colab.

1. Open the notebook in Google Colab.
2. Upload or access the required NASA dataset files.
3. Run the notebook cells in order.
4. Review the generated analyses, tables, and figures.

The dataset is publicly available from NASA OSDR.

## Limitations

The dataset contains only 12 biological samples. The full-data differential-expression results are used as a benchmark reference and should not be considered biological ground truth. Flight and Ground Control animals may also differ in environmental conditions beyond microgravity.

## AI Usage

ChatGPT was used to assist with Python coding and troubleshooting. Claude was used to help explain code and analysis steps and assist with project documentation and report writing.

Details of AI use are documented in [`ai_usage.md`](ai_usage.md).
