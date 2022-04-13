[comment]: <> (Hi. If you are seeing this message, please open this file with markdown preview or jupyter notebook. You can do this by right clicking on the readme file and picking 'open with'.)
# INBRE Google Cloud Training Tutorials

## <a name="overview">Overview</a>

Included here are several tutorials in the form of 'Jupyter notebooks'.

The purpose of these tutorials is to help users familiarize themselves with the cloud computing in the specific context of running bioinformatics workflows.

These tutorials do this by going step-by-step through specific workflows. These workflows cover the start to finish of basic bioinformatics analysis; starting from downloading raw sequence data, and extending to differential gene expression analysis, and producing common plots in R.

## Table of Contents

<a href="#workflow">Workflows</a></br>
<a href="#requirements">Requirements</a></br>
<a href="#getting-started">Getting Started</a></br>
<a href="#data">Data</a></br>
<a href="#funding">Funding</a></br>
</br>

## <a name="workflow">Workflows</a>

Our tutorials are broken down into 'workflows'. Each notebook file covers a specific workflow, which contains written and visual commentary, as well as the actual step-by-step code for running that workflow analysis. 

These notebooks were designed to be run using a virtual machine on a cloud computing provider. For more information on how to do this; navigate to the <a href="#getting-started">'Getting Started'</a> section. You can easily navigate to each of the workflows below by clicking the appropriate link.


![RNA-Seq workflow](images/RNA-Seq_Notebook_Homepage.png)


[Workflow One:](training_demo_short.ipynb) A short introduction to downloading and mapping sequences to a transcriptome using Trimmomatic and Salmon.

[Workflow One (Snakemake):](training_demo_snakemake.ipynb) Using snakemake to run workflow one.

[Extended Workflow One:](training_demo_extended.ipynb) An extended version of workflow one. Once you have got your feet wet, you can retry workflow one with this extended version that covers the entire dataset, and includes elaboration such as using SRA tools for sequence downloading, and examples of running batches of fastq files through the pipeline. This workflow may take around an hour to run.

[Workflow Two:](r_training_demo.ipynb) Using Deseq2 and R to conduct clustering and differential gene expression analysis.



## <a name="requirements">Requirements</a>

These tutorials were designed to be used on cloud computing platforms, with the aim of requiring nothing but the files within this github repository.

With this in mind, our tutorials use Jupyter Notebook files, which Google Cloud Platform, Amazon Web Service, and Microsoft Azure all provide support for. Therefore, requirements should only require creation of a virtual machine on one of these providers, and the downloading of this github's files to that machine.

For more information on creating a virtual machine and downloading our github to that machine, we have a getting started section below. Currently this section only includes information on how to do this using Google Cloud Platform.


## <a name="getting-started">Getting Started</a>

This repository contains several notebook files which serve as bioinformatics workflow tutorials.

The below steps guide you through setting up a virtual machine on Google Cloud Platform, downloading our tutorial files, and running those files.

### Navigating to the Vertex AI Workbench

Once a project has been selected, we can navigate to the Vertex AI Workbench, this is where we can make our virtual machine. 
To get there, select the navigation menu, and navigate to 'Vertex AI' under the Artificial Intelligence section. 
Within the Vertex AI submenu, select 'Workbench'.

![RNA-Seq workflow](images/navigatecircle.png)


### Creating a Virtual Machine

Within the Workbench screen, Select the option to create a 'New Notebook'.

Our notebooks include a notebook that uses R code, so check the 'R' framework. This will include Python as well as R compatibility. You can ignore the advanced options for now, and a default virtual machine will be created with 4 vCPUS and 15GB RAM.

![RNA-Seq workflow](images/newnotebook2.png)

### Starting Your Virtual Machine

To start your virtual machine by clicking 'Open Jupyerlab'. You will know it is running because of the green checkmark.

Note, when you are finished running code, you should turn off your virtual machine to prevent unneeded billing or resource use by checking your notebook and pushing the 'Stop' button. 

![RNA-Seq workflow](images/startingmachine.png)

### Downloading Tutorial Files

Now that you have created your virtual machine, and are in the Jupyterlab screen, you can run our tutorial files. But first you will need to download them.
The easiest way to do this would probably be to clone our repository directly. This can be done by using the 'Git' menu in Jupyterlab, and selecting the clone option. 
Next you can type in the link of repository: "https://github.com/King-Laboratory/rnaseq-myco-notebook.git" (without quotation marks) and click 'Clone'. 

This should download our repo, and the tutorial files inside, into a folder called 'rnaseq-myco-notebook', which you can now navigate to to run our tutorial files.

![RNA-Seq workflow](images/git.png)

### Running Tutorial Files

All our tutorial workflows are are Jupyter format. To run them you need only to navigate to the workflow you want to run in the 'rnaseq-myco-notebook' folder, and double click.
This will open the Jupyter file in Jupyter notebook. From here you can run each 'cell' of the code, one by one, by simplying pushing the 'Play' button on the above menu.

![RNA-Seq workflow](images/runnotebook.png)

### Stopping Your Virtual Machine

When you are finished running code, you can turn off your virtual machine to prevent unneeded billing or resource use by checking your notebook and pushing the 'Stop' button.



## <a name="data">Data</a>

These tutorials use example sequence data procured from the Sally Molloy labratory here at University of Maine; which investigates the transcriptome change in prophage infected, versus non-prophage infected <I>M. chelonae</I> bacteria. The respective article can be found <a href="https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8191103/">here</a>.

## <a name="funding">Funding</a>

Funded by the Maine INBRE Program (NIH/NIGMS P20 GM103423).
