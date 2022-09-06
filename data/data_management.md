# Instructions for Data Management
The two primary types of data needed for this project are student portfolios and their associated metadata (student ID numbers, section numbers, grades). Below are instructions to be shared with faculty so they can retrieve this data from their course sections, as well as instructions for researchers to aggregate the data and prepare for cleaning.

## How to Download Portfolios from Canvas (for Instructors)

1. Starting from the Canvas homepage, click on the section of the course from which you will be collecting student writing. You will be taken to the course homepage. On the left-hand menu, click "Assignments." 
<img width="872" alt="image" src="https://user-images.githubusercontent.com/64552353/188721852-b53c4f1d-db55-484f-9890-d19832e152df.png">
2. Then click the assignment from which the work will be collected (e.g. "Final Portfolio") 
<img width="906" alt="image" src="https://user-images.githubusercontent.com/64552353/188721729-6c6d542e-7d8a-4c34-bedf-2f874186b8f8.png">
3. On the right-hand side of the assignment page, there should be an option to "Download Submissions." Click this button and wait for files to be gathered and downloaded into a zip folder. 
<img width="906" alt="image" src="https://user-images.githubusercontent.com/64552353/188722461-1c032230-9855-4f3c-8341-1152ea60f365.png">
4. Repeat for each course for which you will upload portfolios. Share all Zip files as directed.

## How to Download Grades & Additional Metadata (for Instructors)
Starting from the Canvas homepage, click on the section of the course from which you will be collecting student writing. You will be taken to the course homepage. On the left-hand menu, click "Grades." 
<img width="906" alt="image" src="https://user-images.githubusercontent.com/64552353/188723367-3909d165-ea5d-4281-9331-cf941d120f97.png">

Once in Grades, you will want to filter your Gradebook so the correct metadata can be exported--namely, the grades for the student essays you will be sharing, as everything else (ID numbers, course section) will auto-populate upon export. Depending on how you have set up your Canvas course, filtering may take several forms. 


### Option 1-Filter by Module
1. Click the "View" tab at the top of the Gradebook. From the drop-down menu under view, select "Filters," then "Modules."
<img width="472" alt="image" src="https://user-images.githubusercontent.com/64552353/188724740-8f3f7018-fdb7-4fd1-964a-b94b1934610a.png">
2. From here, you will be able to filter your gradebook so only the assignments from a specific module will appear. On the right-hand side of the Gradebook, a box labed "All Modules" should have appeared. Click the box and select the module that corresponds to the assignment you are submitting student essays from. For example, you may have chosen to make each "week" of your course a module, and the portfolio assignment was due in week 8. 
<img width="232" alt="image" src="https://user-images.githubusercontent.com/64552353/188725200-99d20e50-a057-447c-8e3b-ebc31a34e43b.png">
3. Once you have chosen your module, the gradebook will adjust to show only the grades for the assignment in that week. If there are one or two other assignments in the module, ignore them--these will be eliminated during the aggregation process. Click the "Actions" menu (next to "View") and then select "Export Current Gradebok." 
<img width="275" alt="image" src="https://user-images.githubusercontent.com/64552353/188725633-0b74e75d-21d6-4a79-9173-745b893cd8d4.png">
5. Wait for the csv to download. Open to make sure the following columns have exported: Student ID, Section, and grades corresponding with the relevant assignment. Save the csv and upload to the instructor survey. Repeat for all course sections and share as directed. 

### Option 2-Filter By Module
1. Click the "View" tab at the top of the Gradebook. From the drop-down menu under view, select "Filters," then "Assignment Groups."
<img width="463" alt="image" src="https://user-images.githubusercontent.com/64552353/188726834-9d09e169-987b-4bd3-a6ab-c754ea9cf62d.png">
2. From here, you will be able to filter your gradebook so only the assignments from a specific assignment group will appear. On the right-hand side of the Gradebook, a box labed "All Assignment Groups" should have appeared. Click the box and select the assignment group that corresponds to the assignment you are submitting student essays from. For example, you may have chosen to designate your portfolio as part of its own assignment group called "Final Portfolio." 
<img width="234" alt="image" src="https://user-images.githubusercontent.com/64552353/188727097-73eadc47-61fb-434a-8ef0-6d9545037130.png">
3. Once you have chosen your assignment group, the gradebook will adjust to show only the grades for the assignment in that group. If there are one or two other assignments in the module, ignore them--these will be eliminated during the aggregation process. Click the "Actions" menu (next to "View") and then select "Export Current Gradebook." 
<img width="275" alt="image" src="https://user-images.githubusercontent.com/64552353/188725633-0b74e75d-21d6-4a79-9173-745b893cd8d4.png">
4. Wait for the csv to download. Open to make sure the following columns have exported: Student ID, Section, and grades corresponding with the relevant assignment. Save the csv and upload to the instructor survey. Repeat for all course sections and share as directed. 

### Option 3-No Filters: 
1. If the filters will not reduce your Gradebook to the parameters specified, simply click "Actions" and select "Export Entire Gradebook." 
2. Wait for the csv to download. Open to make sure the following columns have exported: Student ID, Section, and grades corresponding with the relevant assignment. Ignore all other sections--they will be removed during aggregation and cleaning. Save the csv and upload to the instructor survey. Repeat for all course sections and share as directed. 

**WARNING:** Please do NOT upload a plain CSV file with ONLY the instructor grades in lieu of the Canvas spreadsheet! In order for the cleaning and aggregation pipeline to work, student IDs and course sections are needed in the EXACT FORMAT generated by the Canvas spreadsheet. You are welcome to remove additional columns from the Canvas spreadsheet before submitting it to me, but you are not required to--all of these will be automatically removed by the code. If you have questions or are having trouble downloading the spreadsheet, please reach out to me at megan.kane@temple.edu

## How to Aggregate Portfolios and Metadata (for Researchers)

**Portfolios:** Download all ZIP folders and extract all student portfolios into a SINGLE folder on local machine. Run the following code to convert all documents in the file to txt files: `textutil -convert txt /path/to/DOCX/files/*.docx`  

**Metadata*:** Download all csv files and consolidate into one master file using the Excel consolidate method OR dataframe.append in Python (need to test to see which is easier for multiple files). 
