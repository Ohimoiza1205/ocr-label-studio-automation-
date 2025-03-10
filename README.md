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
- [License](#license)
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
Invoice-Annotation-Project/ 
├── README.md 
  ### Project documentation 
  ├── invoice_label_config.xml 
  ### XML configuration for Label Studio 
  ├── invoice_ocr_output.json 
  ### OCR output JSON file (generated via Colab) 
  ├── label_studio_output.json 
  ### Final annotated JSON from Label Studio 
  ├── document_analysis.txt 
  ### Bullet list of identified fields 
  └── reflection.md


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

# Invoice Annotation Project: Step-by-Step Instructions

## Step 1: Document Analysis & Label Identification
**Task:**  
Review the sample invoice image and identify key fields.

**Deliverable:**  
A bullet list of fields saved in `document_analysis.txt`.

**Example:**
- Invoice Number
- Invoice Date
- Customer Name
- Item Descriptions
- Quantity, Unit Price
- Tax
- Total Amount


---

## Step 2: XML Label Configuration
**Task:**  
Create an XML configuration file for Label Studio to define the labels for annotation.

**Deliverable:**  
Save the following as `invoice_label_config.xml`.

**Example:**
```xml
<View>
  <Image name="image" value="$image" zoom="true" />
  <RectangleLabels name="label" toName="image">
    <Label value="Invoice Number" background="blue" />
    <Label value="Invoice Date" background="green" />
    <Label value="Customer Name" background="yellow" />
    <Label value="Item Descriptions" background="orange" />
    <Label value="Quantity, Unit Price" background="red" />
    <Label value="Tax" background="pink" />
    <Label value="Total Amount" background="purple" />
  </RectangleLabels>
  <TextArea name="transcription" toName="image" editable="true" perRegion="true"
            rows="3" placeholder="Enter recognized text here" />
</View>
```
## Step 3: Generate OCR Data

**Task:**  
Run the provided Google Colab Notebook to extract text and bounding boxes from the sample invoice.

**Instructions:**  
1. Open the Pre-Configured Colab Notebook.  
2. Update the `image_url` variable to:
   ```bash
   https://allies-assets.s3.us-east-1.amazonaws.com/birthplan_builder_assets/extra_images/invoice_sample.png
3. Click Runtime > Run all to execute all cells.
4. When prompted (or via the Files sidebar), download the generated file as invoice_ocr_output.json.
- Deliverable:
invoice_ocr_output.json

## Step 4: Label Refinement in Label Studio

**Task:**
Import the OCR JSON file into Label Studio, refine the bounding boxes, correct OCR text, and assign the correct labels.

**Instructions:**
1. Launch Label Studio at http://localhost:8080 and create a new project named "Invoice Annotation."
2. In the project settings, paste the XML configuration from Step 2 and click Save.
3. Import the invoice_ocr_output.json file into your project.
4. Open the task, adjust bounding boxes, delete any irrelevant annotations, and manually correct any OCR errors.
5. Once satisfied, export the final labeled dataset as label_studio_output.json.
- Deliverable:
label_studio_output.json

## Step 5: Reflection and Final Report

**Task:**
Write a reflection (150–200 words) discussing:

1. Label Selection: Why you chose the specific labels.
2. Challenges: What issues you encountered during OCR and annotation, and how you addressed them.
3. Workflow Improvements: Suggestions for streamlining the process in the future.
- Deliverable:
Save your reflection in reflection.md.

## License
This project is licensed under the MIT License.

## Contact
For any questions, please contact [omoiza@ttu.edu].
