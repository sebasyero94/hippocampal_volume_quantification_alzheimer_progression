# hippocampal_volume_quantification_alzheimer_progression

This project is an end-to-end AI system which features a machine learning algorithm that integrates into a clinical-grade viewer and automatically measures hippocampal volumes of new patients, as their studies are committed to the clinical imaging archive.

## Model
This segmentation algorithm is based on the [U-Net architecture](https://lmb.informatik.uni-freiburg.de/people/ronneber/u-net/).

## The Dataset
We are using the "Hippocampus" dataset from the [Medical Decathlon competition](http://medicaldecathlon.com/). This dataset is stored as a collection of NIFTI files, with one file per volume, and one file per corresponding segmentation mask. The original images here are T2 MRI scans of the full brain. As noted, in this dataset we are using cropped volumes where only the region around the hippocampus has been cut out. 
HippoCrop images in the dataset are the rectangular cut out portion of a brain scan from every image series radiologists have collected and annotated a dataset of relevant volumes, and converted them to NIFTI format.

### Workflow
The model integrates into a working clinical PACS such that it runs on every incoming study and produces a report with volume measurements.

## Details
Section1 = Exploratory Data Analysis
Section2 = Train
Section 3 = Run in workflow

## Background

Alzheimer's disease (AD) is a progressive neurodegenerative disorder that results in impaired neuronal (brain cell) function and eventually, cell death. AD is the most common cause of dementia. Clinically, it is characterized by memory loss, inability to learn new material, loss of language function, and other manifestations.

For patients exhibiting early symptoms, quantifying disease progression over time can help direct therapy and disease management.

A radiological study via MRI exam is currently one of the most advanced methods to quantify the disease. In particular, the measurement of hippocampal volume has proven useful to diagnose and track progression in several brain disorders, most notably in AD. Studies have shown a reduced volume of the hippocampus in patients with AD.

The hippocampus is a critical structure of the human brain (and the brain of other vertebrates) that plays important roles in the consolidation of information from short-term memory to long-term memory. In other words, the hippocampus is thought to be responsible for memory and learning (that's why we are all here, after all!)

![hippo_small](https://video.udacity-data.com/topher/2020/March/5e813bf9_hippocampus-small/hippocampus-small.gif)
Source: Life Science Databases (LSDB). Hippocampus. Images are from Anatomography maintained by Life Science Databases (LSDB). (2010). CC-BY-SA 2.1jp


Humans have two hippocampi, one in each hemisphere of the brain. They are located in the medial temporal lobe of the brain. Fun fact - the word "hippocampus" is roughly translated from Greek as "horselike" because of the similarity to a seahorse observed by one of the first anatomists to illustrate the structure, but you can also see the comparison in the following image.

![2](https://video.udacity-data.com/topher/2020/March/5e813bf7_hippocampus-and-seahorse-cropped/hippocampus-and-seahorse-cropped.jpg)

the volume of hippocampus varies in a population, depending on various parameters, within certain boundaries, and it is possible to identify a "normal" range taking into account age, sex and brain hemisphere.

You can see this in the image below where the right hippocampal volume of women across ages 52 - 71 is shown.

![3](https://video.udacity-data.com/topher/2020/March/5e813c01_nomogram-fem-right/nomogram-fem-right.jpg)
Nomogram - Female, Right Hippocampus Volume, Corrected for Head Size
Source: Nobis, L., Manohar, S.G., Smith, S.M., Alfaro-Almagro, F., Jenkinson, M., Mackay, C.E., Husain, M. Hippocampal volume across age: Nomograms derived from over 19,700 people in UK Biobank. Neuroimage: Clinical, 23(2019), pp. 2213-1582.


---
This project is based on the curricula offered by Udacity in its AI in Healthcare Nanodegree program.
