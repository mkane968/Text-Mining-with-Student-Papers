# Text Mining with Student Papers
Python script for processing and analyzing textual features extracted from student essays. 

## Data Collection
To use these scripts, you will need a corpus of student writing--a folder of individual essays in txt format works best. You will also need a CSV file with metadata for each essay, including student ID, course section, and essay score. See `/data` folder for examples.

Collecting writing from instructors? See the [template for data collection](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/data/data_collection.md) in the `/data` folder of this repository.

## Data Conversion
Data must be in the following formats: 
* Student writing = .txt
* Grade metadata = .csv

If student essays are originally in docx format, conversion to txt is necessary. To convert docx to text (without including page numbers and other headers/footers), use the following command in terminal: `textutil -convert txt /path/to/DOCX/files/*.docx` 

Convert individual files from docx (or any other file extension) to text by going to "File -> Save As ->" and selecting txt as extension. Do this if small batch of files  has different extension like .pages or .pdf. 

## Using the Code
Clean and merge all text files and metadata using [this script.](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Clean%20and%20Merge%20Essays%20%26%20Metadata.ipynb)
