# Supereffectors_scRNAseq

------------------------------------------------------------------------
This repository contains analysis of scRNAseq data for the manuscript by Tsyklauri et al., 2022. 

------------------------------------------------------------------------
## LICENSE: MIT License.

All scripts are distributed to ease the reproduction of the analysis
from the above paper, but WITHOUT ANY WARRANTY; without even the 
implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. 
See the MIT Licence and LICENSE.md file for more details.

**Manuscript:** LINK

**Deposited data:** LINK

## Requirements

You need R 4.0.3 with following packages:
* Seurat 4.0.0
* rmarkdown
* ggplot
* dplyr
* tibble

You need also Cellranger 5.0.0, as well as a software that can open 
tar.gz.files.

------------------------------------------------------------------------

## PART 1:
- Pre-mapping of with cellranger:
	- Cellranger 5.0.0 with default parameters
	- Feature barcode reference: file FeatureReference.csv
	- Reference tanscriptome Mouse GRCm38, version 102 downloaded from Ensembl
- Extraction of the used samples based on Cell Hashtags on pre-mapped files:  
	
	- Extraction of barcodes separated by Hashtags:
		- Uses script: Supereffectors_PART1_1_generating_sample_lists.Rmd
	- Demultiplexing of fastq files using said Hashtag files:
		- Uses script: Supereffectors_PART1_2_demultiplexing.py  
	    **Note:** If you have downloaded fastq files from link above this
	    does not have to be ran, as those fastqs are already demultiplexed.
	    You still need to run the script above to generate hashtag lists though, but in that case use it only for data annotation and meta data creation.
	- Mapping with cellranger:
		- Same parameters are used as for pre-mapping.
	- Preparation of first version of data set: 
		- Uses script: Supereffectors_PART1_3_Initial_analysis.Rmd

- For detailed information please see each script.


## PART 2:
- Quality control and filtering
- Normalization, dimensionality reduction, clustering

- For detailed information please see each script.

<!-- ## PART 3:

 - All figures for the manuscript -->

------------------------------------------------------------------------
