Image Segmentation and Analysis Using CellProfiler, Ilastik, and ImageJ

Introduction

This project focuses on the segmentation of images of the substantia nigra, a brain region critical in Parkinson’s disease research. The goal is to create a robust image processing pipeline using Ilastik, ImageJ, and CellProfiler to improve binary image quality and accurately calculate Regions of Interest (ROI), such as cell counting. This pipeline enables precise quantification of cellular structures, which is essential for studying disease progression.

Tools Used

ImageJ: A versatile image processing software with extensive plugins for deep learning-based analysis.

Ilastik: A user-friendly tool for pixel and object classification, supporting both traditional machine learning and deep learning workflows.

CellProfiler: An open-source software designed for automated cell image analysis, enabling segmentation and data extraction.

Workflow Overview

Image Segmentation with Ilastik:

Train the model by manually annotating a subset of images.

Use the trained model to classify and segment cell structures.

Export the segmented image as a .tif file.

Binary Mask Conversion with ImageJ:

Load the .tif file into ImageJ.

Convert the segmented image to a binary mask (cells in white, background in black).

Quantification with CellProfiler:

Import the binary mask into CellProfiler.

Configure the pipeline to identify and count ROIs.

Export the results as a spreadsheet.

Dataset Organization

Dataset Folder: Store all images in a folder named datasets on the desktop.

Naming Convention: Save processed images with descriptive filenames (e.g., dataset1.tif).

Step-by-Step Guide

Image Preprocessing (Optional, using ImageJ)

Open ImageJ and load the image.

Crop the image (if necessary).

Save the cropped image in the datasets folder.

Segmentation with Ilastik

Open Ilastik and create a new Pixel Classification project.

Load the image from the datasets folder.

Annotate a few cells as "Foreground" (yellow) and some background areas as "Background" (blue).

Train the model and use live updates to refine results.

Export the segmentation as a .tif file.

Binary Mask Generation with ImageJ

Load the .tif file into ImageJ.

Adjust contrast and convert the image to an 8-bit grayscale.

Convert the grayscale image into a binary mask.

ROI Counting with CellProfiler

Without Batch Processing

Load the binary mask into CellProfiler.

Extract metadata and set image type to "Binary Images".

Identify primary objects and analyze images.

With Batch Processing

Load multiple images from the dataset folder.

Extract metadata and select binary images.

Configure object processing and set thresholds.

Export the results as a spreadsheet.

Results

The final spreadsheet contains quantitative data on cell counts.

The pipeline ensures high accuracy in identifying and segmenting cellular structures.

Conclusion

This project successfully segments and quantifies cells using Ilastik, ImageJ, and CellProfiler. The automated workflow enhances the accuracy of image analysis, making it a valuable tool for Parkinson’s disease research and other biomedical applications.

Repository Structure

📂 Image-Segmentation-Analysis
 ├── datasets/         # Raw and processed image datasets
 ├── scripts/          # Scripts for automation (if applicable)
 ├── results/          # Exported spreadsheets and analysis
 ├── README.md         # Project documentation

Acknowledgments

This project leverages open-source tools to facilitate biomedical image analysis. Special thanks to the developers of ImageJ, Ilastik, and CellProfiler for their contributions to scientific research.
