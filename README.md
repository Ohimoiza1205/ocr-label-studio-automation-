# Invoice Annotation Project

This repository contains all the code, configuration files, and documentation for the Invoice Annotation Project. The objective is to build an end-to-end workflow for processing a sample invoice using OCR, refining annotations with Label Studio, and preparing a dataset for AI training.

## Table of Contents
- [Overview](#overview)
- [Project Workflow](#project-workflow)
- [Repository Structure](#repository-structure)
- [Requirements](#requirements)
- [Setup and Installation](#setup-and-installation)
- [Step-by-Step Instructions](#step-by-step-instructions)
  - [Step 1: Document Analysis & Label Identification](#step-1-document-analysis--label-identification)
  - [Step 2: XML Label Configuration](#step-2-xml-label-configuration)
  - [Step 3: Generate OCR Data](#step-3-generate-ocr-data)
  - [Step 4: Label Refinement in Label Studio](#step-4-label-refinement-in-label-studio)
  - [Step 5: Reflection and Final Report](#step-5-reflection-and-final-report)
- [Licence](#license)
- [Contact](#contact)

## Overview

The project demonstrates:
- Extraction of text from a scanned invoice using Tesseract OCR.
- Creation of a custom XML configuration for Label Studio.
- Refinement of OCR output and manual labeling of invoice fields.
- Compilation of a final annotated dataset and a reflection on the process.

## Project Workflow

1. **Document Analysis & Label Identification:** Identify key invoice fields.
2. **XML Label Configuration:** Create an XML file to define labels for annotation.
3. **Generate OCR Data:** Use a Colab Notebook to extract text and bounding boxes.
4. **Label Refinement in Label Studio:** Import and refine annotations.
5. **Reflection and Final Report:** Write a reflection on your process and improvements.

## Repository Structure
Invoice-Annotation-Project/ ├── README.md # Project documentation ├── invoice_label_config.xml # XML configuration for Label Studio ├── invoice_ocr_output.json # OCR output JSON file (generated via Colab) ├── label_studio_output.json # Final annotated JSON from Label Studio ├── document_analysis.txt # Bullet list of identified fields └── reflection.md


## Requirements

- Python 3.7+  
- Tesseract OCR (installed and in your PATH)  
- Google Colab account (for running the OCR notebook)  
- Label Studio (installed locally)

## Setup and Installation

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/yourusername/Invoice-Annotation-Project.git
   cd Invoice-Annotation-Project

2. **Install Label Studio:**
```bash
pip install label-studio
label-studio start
```
3. **Set Up Tesseract OCR:**
Follow instructions for your OS to install Tesseract OCR.

Contact
For any questions, please contact ![omoiza@ttu.edu].
