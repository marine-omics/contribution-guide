# Marine Omics Contribution Guide

All projects in Marine Omics should aim to be *publication ready* almost from the first commit.  In essence this means that;

- Anyone who finds the project should be able to check it out, follow the README and run it
- The project should be complete in the sense that instructions are provided for obtaining all raw data and running any analyses not included in the repository
- The project should be clean in the sense that it contains only the files needed to run the analyses


## Workflow

In general you should not be pushing changes directly to any projects in `Marine Omics`.  To contribute you should follow this workflow instead

1. Create a private [Fork](https://help.github.com/articles/fork-a-repo/) of the project
2. Clone your private fork to your computer and make changes
3. Push changes to your private fork until you are happy with the result
4. Make a pull request to have your changes merged back with the master `Marine Omics` repo.  Assign someone other than yourself to review the pull request

You should not merge your own pull requests as the point of this workflow is to encourage code review by others.

## Keeping your fork in sync

If more than one person is making edits to a repository it is important to always ensure you are editing the most recent version in order to minimise the potential for merge conflicts. Before making edits you can make sure that your private fork is up to date with the latest changes by closely following the github instructions for [syncing a fork](https://help.github.com/articles/syncing-a-fork/).  

## Data Projects

A data project is typically a mix of data files, scripts for processing those files and code for analysing and visualising. To make your data project readable by others it is important to follow standard conventions for organising these files into folders.  For *Marine Omics* projects you should start by using [this template](https://github.com/marine-omics/project-template)



## Managing Large Files

In 'Omics type projects one of the principle challenges is managing large data files.  Because these large files cannot be easily checked in to git they need to be managed manually.  Please use the following conventions for managing these types of files. 

- **Include a download link** for any large files that you place in the `raw_data` directory of your project.  Various services like [DropBox](www.dropbox.com) and [Google Drive](drive.google.com) allow you to create downloadable URLs for large files but if you don't have access to these service or enough space in your account there are free alternatives available through the Australian research cloud.

- **Include a script** to generate any intermediate files that feature in your code.  For example if you have R code that reads an intermediate file your code should check for the presence of that file and if it is missing it should output a message telling the user how to obtain the file (eg by running the script).

- **Document your HPC workflow** within the `HPC` directory of your project.  Make sure you include any scripts and batch files describing your HPC workflow and instructions on how to obtain the raw data.  Anyone who checks out your project should be able to read these instructions and rerun your analysis to bootstrap the project.

