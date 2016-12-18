# Marine Omics Contribution Guide

All projects in Marine Omics should aim to be *publication ready* almost from the first commit.  In essence this means that;

- Anyone who finds the project should be able to check it out, follow the README and run it
- The project should be complete in the sense that instructions are provided for obtaining all raw data and running any analyses not included in the repository
- The project should be clean in the sense that it contains only the files needed to run the analyses


## Data Projects

A data project is typically a mix of data files, scripts for processing those files and code for analysing and visualising. To make your data project readable by others it is important to follow standard conventions for organising these files into folders.  For *Marine Omics* projects you should start by using [this template]()



## Managing Large Files

In 'Omics type projects one of the principle challenges is managing large data files.  Because these large files cannot be easily checked in to git they need to be managed manually.  Please use the following conventions for managing these types of files. 

- **Include a download link** for any large files that you place in the `raw_data` directory of your project.  Various services like [DropBox](www.dropbox.com) and [Google Drive](drive.google.com) allow you to create downloadable URLs for large files but if you don't have access to these service or enough space in your account there are free alternatives available through the Australian research cloud.

- **Include a script** to generate any intermediate files that feature in your code.  For example if you have R code that reads an intermediate file your code should check for the presence of that file and if it is missing it should output a message telling the user how to obtain the file (eg by running the script).

- **Document your HPC workflow** within the `HPC` directory of your project.  Make sure you include any scripts and batch files describing your HPC workflow and instructions on how to obtain the raw data.  Anyone who checks out your project should be able to read these instructions and rerun your analysis to bootstrap the project.

