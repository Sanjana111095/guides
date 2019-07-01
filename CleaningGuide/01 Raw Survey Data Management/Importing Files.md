## Importing into Stata
Data comes in many forms, from raw text (.txt) files to multi-sheet Excel files. Importing data into Stata is necessary if the data is not already in Stata format (.dta file). In general, you should be able to use Stata’s functions and loops to efficiently import data. Stata can import most data formats. If your project’s data was collected using a platform like SurveyCTO, the raw data will come in .csv format. See the data collection folder for detailed instructions on importing SurveyCTO data. 

## Importing from different sources 
In Stata 13 and beyond, the import command can import CSV files, excel files, and more depending on the option used (delimited for CSV, excel for excel), and export does the same for exporting. If you are new to using import or are importing a file type you have not seen before, it can be helpful to use the drop-down menu by clicking “file>Import” and then selecting the file type most like yours. Once you do this, you will be able to copy the specific command syntax directly from the command prompt or review window in Stata to your script.  
Note that it is often a good idea when using the insheet command, to use the option names and have your dataset have the same variable names at those at the top of the raw dataset.

A useful function for importing multiple files within a folder is the dir extended macro function. You can find documentation on this by typing help extended_fcn in Stata.  This function allows you to store all the names of the files in a folder in a local so you can loop through them for importing. See an example script of this process below. 