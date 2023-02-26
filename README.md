# Methods Snack: Dimension reduction methods for single-cell RNA-sequencing data. 

This repository hosts a Jupyter notebook with an interactive introduction to popular dimension reduction methods for single-cell RNA-seq data, including explanations and code demos, in parts adapted from this [scanpy tutorial](https://scanpy-tutorials.readthedocs.io/en/latest/pbmc3k.html#)

The notebook was created for a "Methods Snack" lecture in the [MeInBio graduate programme](https://www.meinbio.uni-freiburg.de), given on February 27, 2023. 

## Introduction 

One of the first steps in a typical single-cell RNA-seq data analysis workflow is to reduce dimensionality to be able to look at your data. Among the most popular approaches are PCA, tSNE, UMAP, or deep-learning based methods. If you have you ever wondered how to choose one method over the other, how they really work “under the hood” and how to know which parameters to pick when applying them, this method snack might be for you. 
I will introduce the inner workings of PCA, tSNE, UMAP and autoencoders (a deep learning-based technique), and provide some considerations to take into account when choosing a method for dimension reduction based on your dataset and your specific research question. Throughout the methods snack, we’ll be working with hands-on examples in Python in a Jupyter notebook, to see the methods “in action”, compare them to one another on different datasets, and gain some insights on how to select parameters. This repository hosts the notebook. In this README, you can find some instructions on how to access and use it. 

## Instructions for using the notebook 

### **Option 1: Run the notebook on Google Colab**

<a href="https://colab.research.google.com/github/maren-ha/DimensionReductionForScRNASeq/blob/main/DimensionReduction_Colab.ipynb" target="_parent"><img src="https://colab.research.google.com/assets/colab-badge.svg" alt="Open In Colab"/></a> 

* ***Prerequisites:*** You need a Google account (and a small bit of free space on your Google Drive). 
* ***Pros:*** Requires no local installation of Python or any packages
* ***Cons:*** Relatively low compute power, i.e., slow runtime. 
* ***Instructions:***
  * get a copy of the notebook to your Google Drive: Open the notebook and create a copy in your Google Drive 
> :zap: **Very important**:zap: Please make a copy of the notebook straight away or upload the `DimensionReduction_Colab.ipynb` file from the repository to your Google Drive, so that you have a copy in your own Google Drive! Make sure to make changes only to the copy, otherwise you will not be able to save it and any changes you do in the notebook will be lost after you close the browser tab. 

### **Option 2: Run the notebook on Jupyter**

This requires to run the notebook locally, you need Python and Jupyter installed on your laptop. You can follow these steps:  

1) **Install Python:** https://wiki.python.org/moin/BeginnersGuide/Download

2) a) **Install Jupyter for Linux and Mac OS**
 - go to: https://pip.pypa.io/en/stable/installation/
    or search: “install pip” and select the first link
 - download: “get-pip.py” (https://bootstrap.pypa.io/get-pip.py) into you folder, e.g., Downloads
 - open the terminal and type
    ``` 
    > cd ~/Downloads
    > python get-pip.py --user
    > /home/username/.local/bin/pip install jupyter --user
    > git clone https://github.com/maren-ha/DimensionReductionForScRNASeq.git
    > cd DimensionReductionForScRNASeq
    ```
 - to start a jupyter notebook, type: 
    ``` 
    /home/username/.local/bin/jupyter notebook
    ```
 - in Jupyter, navigate to the folder where you downloaded the git repo

2) b) **Install Python and Jupyter for Windows**

All windows users can download and install the software from the following link: https://www.anaconda.com/products/individual#windows. It includes both a python 3.8 and a jupyter notebook installation. For starting up jupyter, you can open the anaconda navigator and launch the software which should open a link in your browser.
