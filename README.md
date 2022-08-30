# Text-Mining-with-Student-Papers
Python script for processing and analyzing textual features extracted from student essays. 

## Preliminaries

To use these scripts, you will need a corpus of student writing--it will likely be a folder of individual essays in docx format donwloaded from Canvas. 

Batch convert all files in a folder from docx to txt using the following command in terminal: `textutil -convert txt /path/to/DOCX/files/*.docx`  

Can also convert individual files from docx (or any other file extension) to text by going to "File -> Save As ->" and selecting txt as extension. Do this if small batch of files  has different extension like .pages or .pdf. 

In either case, page numbers and other headers will NOT be included in converted documents. 

Load plain text files into this script for preprocessing and cleaning: https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Uploading_and_Cleaning_Student_Essays_&_Metadata.ipynb
