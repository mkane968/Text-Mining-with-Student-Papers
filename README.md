# Text Mining with Student Papers
Python script for processing and analyzing textual features extracted from student essays. 

## Preliminaries

To use these scripts, you will need a corpus of student writing--a folder of individual essays in txt format works best. 

*Collecting writing from instructors? See the [template for data collection](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/data/data_management.md) in `/data` folder of this repository.*

To convert all files in a folder from docx to txt, use the following command in terminal: `textutil -convert txt /path/to/DOCX/files/*.docx`  

You can also convert individual files from docx (or any other file extension) to text by going to "File -> Save As ->" and selecting txt as extension. Do this if small batch of files  has different extension like .pages or .pdf. 

In any case, page numbers and other headers will NOT be included in converted documents. 

You will also need a CSV file with metadata for each essay, including student ID, course section, and essay score. See data folder for example. 

Load plain text files and metadata into [this script](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Clean%20and%20Merge%20Essays%20%26%20Metadata.ipynb) in the `/notebooks` folder of this repository to clean and merge.
