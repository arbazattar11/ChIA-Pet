# ChIA-PET Data Analysis Pipeline

This pipeline is designed to analyze ChIA-PET sequencing data. Below are the steps involved:

1. **Quality Control (QC):**
   - FASTQ files are checked for quality using FastQC, and a summary report is generated using MultiQC.

2. **Read Alignment:**
   - Reads are aligned to the reference genome using BWA.

3. **Mapping Filtering:**
   - Unmapped reads, PCR duplicates, and low-quality mappings are filtered out using samtools.

4. **Peak Calling (Optional):**
   - ChIA-PET does not typically involve peak calling as in ChIP-seq analysis.

5. **Interaction Calling:**
   - Chromatin interactions are identified using ChIA-PET specific algorithms like chiasig.

6. **Annotation and Visualization:**
   - Identified interactions are annotated with genomic features using annotatePeaks.pl, and a profile plot is generated.

7. **Differential Interaction Analysis (Optional):**
   - Differential interaction analysis can be performed if comparing between different experimental conditions.

8. **Functional Enrichment Analysis:**
   - Perform functional enrichment analysis of interacting regions using external tools like GREAT or Enrichr.

9. **Visualization and Interpretation:**
   - Visualize and interpret the identified chromatin interactions to gain insights into regulatory mechanisms.

## Usage
- Clone this repository.
- Place your FASTQ files in the same directory as the pipeline script.
- Modify the script as necessary to specify paths and parameters.
- Run the pipeline using `./pipeline.sh`.

## Requirements
- BWA
- Samtools
- FastQC
- MultiQC
- deeptools (for annotatePeaks.pl and plotProfile)
- External tools for functional enrichment analysis

## Notes
- Adjust parameters and additional analysis steps based on specific experimental needs.
- Ensure reference genome files are available and properly indexed.
