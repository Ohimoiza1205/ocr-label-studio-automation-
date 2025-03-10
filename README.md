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
- [How to Submit](#how-to-submit)
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

