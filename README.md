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

## Using the Code
Associate all student essays with their metadata using [this script.](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Merge_Student_Essays_%26_Metadata.ipynb)

Perform basic cleaning and exploratory text mining on essays using this script.
