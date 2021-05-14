# NanoString GeoMx DSP

This project contains worked examples processing NanoString GeoMx digital count conversion (DCC) files generated from the GeoMx NGS Pipeline on the Illumina DRAGEN platform.  The NanoString GeoMx DSP workflow sequences aspirated DNA oligos tagging RNA transcripts in either commercially available (e.g., whole transcriptome and others, found [here](https://www.nanostring.com/products/geomx-digital-spatial-profiler/geomx-rna-assays/)) or custom-designed RNA assay panels.  

The following directories and files are included in this project:

* `DCC_Files`: three example DCC files (`DSP-Demo-A-A01.dcc`, `DSP-Demo-A-A02.dcc`, and `DSP-Demo-A-A03.dcc`).  The DCC files contain all the digital counts for each region of interest (ROI) or segment in a tissue sample for all targets, which are defined by the Readout Tag Sequence (RTS ID).  

* `DRAGEN_Files`: contains `Input` subdirectory with all of the RTS sequences (`RTS_sequences.txt`), a comma-separated value file with the cloud locations of read 1 and read 2 FASTQ files for each demo sample (`fastq_list.csv`), and a sample ID list required for the digital count conversion, in JavaScript-object notation format (`sample_id_list.json`).  Additionally, the `Output` subdirectory contains all of the Illumina DRAGEN output files for each sample (i.e., `DSP-Demo-A-A01`, `DSP-Demo-A-A02`, and `DSP-Demo-A-A03`) including average and per-base summary statistics for each read, and other useful metrics.

* `summary.txt`: contains the summary metrics for each demo sample, including the number of raw, trimmed, stitched, aligned (not applicable in this workflow), and total number of deduplicated reads.  

* `FASTQ`: contains the compressed (`.gz`) R1 and R2 FASTQ files for each sample.

* `Demo_Configuration.ini`: configuration file from the NanoString GeoMx DSP instrument used as input for the GeoMx DSP NGS Pipeline with Illumina DRAGEN to generate DCC files.  The configuration file contains summary information on the instrument model and read pattern (e.g., 27x27 for paired-end 27-cycle chemistry), the adapter sequences used, and the targets (RTS numbers and associated sequences).

