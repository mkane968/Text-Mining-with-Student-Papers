# Text Mining with Student Papers
This repository includes instructions and Python scripts for processing and analyzing textual features extracted from student essays. 

## About The Project
This repository lets users clean, explore and analyze student academic essays through a multi-step pipeline.

First, any given corpus of student essays can be merged into single dataframe and  associated with their metadata in a master dataframe.

Then, basic cleaning and enrichment can be performed on the corpus. 

Using a combination of natural language processing techniques, each essay can then be searched for **key words and phrases** associated with students' **uptake of certain first-year writing program outcomes.** Examples include: 
*   `Rhetorical analysis terms like "pathos" , "ethos" , "logos"` &rarr; *To learn to employ rhetorical terms and strategies and strengthen your ability to analyze rhetorical techniques in published essays and visual texts.*
*   `Regular expressions associated with in-text citations` &rarr; *To learn to employ academic evidence*
*   `Terms from stance word dictionary` &rarr; *To develop competent academic arguments over multiple drafts*

*Outcomes from ENG 701 Syllabus, Temple University First-Year Writing Program, Revised June 2022*

Once texts have been searched for these outcomes, their surrounding context can be retrieved and stored for further analysis. Since each text is associated with its grade metadata, researchers can investigate trends in language patterns and their differences; for example, across high (A), mid-range (B-C) and low-scoring (D-F) essays. This can be done using natural-language processing tools in this repository as well as by using [the DocuScope tool.](https://www.cmu.edu/dietrich/english/research-and-publications/docuscope.html)


## Data Collection
To use these scripts, you will need a corpus of student writing--a folder of individual essays in txt format works best. You will also need a CSV file with metadata for each essay, including student ID, course section, and essay score. See `/data` folder for examples.

Collecting writing from instructors? See the [guide to data collection for instructors and researchers](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/data/data_collection.md) in the `/data` folder of this repository.

## Data Conversion
Data must be in the following formats: 
* Student writing = .txt
* Grade metadata = .csv

If student essays are originally in docx format, conversion to txt is necessary. To convert docx to text (without including page numbers and other headers/footers), use the following command in terminal: `textutil -convert txt /path/to/DOCX/files/*.docx` 

Convert individual files from docx (or any other file extension) to text by going to "File -> Save As ->" and selecting txt as extension. Do this if small batch of files  has different extension like .pages or .pdf. 

## Code Usage (Work in Progress)
[**Master Pipeline**](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Student_Essay_Text_Mining_Master_Pipeline.ipynb): Contains all steps from uploading initial files to sectioning and analyzing texts based on evidence of outcomes uptake.

[**Associate Student Essays and Metadata**](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Associate_Student_Essays_%26_Metadata.ipynb): Merge all student essays into single dataframe, associate with their metadata in a master dataframe and download as a tsv file.

[**Preprocessing & Basic Text Analysis**](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Preprocessing_and_Basic_Text_Analysis.ipynb): Perform basic cleaning and exploratory text mining using tsv file of student essays associated with metadata. 

[**Section Texts Based on Outcomes**](https://github.com/mkane968/Text-Mining-with-Student-Papers/blob/main/notebooks/Section_Texts_Based_on_Outcomes.ipynb): Perform text sectioning and analysis based on outcomes related to rhetorical analysis, citation and argumentation 
