# Text Mining with Student Papers
This repository includes instructions and Python scripts for processing and analyzing textual features extracted from student essays. 

## Data Collection
To use these scripts, you will need a corpus of student writing--a folder of individual essays in txt format works best. You will also need a CSV file with metadata for each essay, including student ID, course section, and essay score. See `/data` folder for examples.

Collecting writing from instructors? See the [guide to data collection for instructors and researchers](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/data/data_collection.md) in the `/data` folder of this repository.

## Data Conversion
Data must be in the following formats: 
* Student writing = .txt
* Grade metadata = .csv

If student essays are originally in docx format, conversion to txt is necessary. To convert docx to text (without including page numbers and other headers/footers), use the following command in terminal: `textutil -convert txt /path/to/DOCX/files/*.docx` 

Convert individual files from docx (or any other file extension) to text by going to "File -> Save As ->" and selecting txt as extension. Do this if small batch of files  has different extension like .pages or .pdf. 

## Code Usage
[**Associate Student Essays and Metadata**](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Associate_Student_Essays_%26_Metadata.ipynb): Mege all student essays into single dataframe, associate with their metadata in a master dataframe and download as a tsv file.

[**Preprocessing & Basic Text Analysis**](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Preprocessing_and_Basic_Text_Analysis.ipynb): Perform basic cleaning and exploratory text mining using tsv file of student essays associated with metadata. 

[**Section Texts Based on Outcomes**](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Section_Texts_Based_on_Outcomes.ipynb): Perform text sectioning and analysis based on outcomes related to rhetorical analysis, citation and argumentation (Work in Progress)
