# Document Scanner and OCR

## 📌 Project Overview
This project implements an automated **Computer Vision and OCR (Optical Character Recognition) pipeline** designed to ingest physical documents or unstructured image data and transform them into structured, machine-readable text. 

## 🏗️ Data Pipeline Architecture

The pipeline processes data through the following automated stages:

### 1. Data Ingestion & Preprocessing
* **Image Loading:** Reads raw unstructured image data.
* **Noise Reduction & Normalization:** Applies grayscale conversion and Gaussian blurring via OpenCV to reduce noise and standardize the input data for feature extraction.

### 2. Transformation (Feature Engineering)
* **Edge Detection:** Utilizes the Canny Edge Detection algorithm to map the structural boundaries of the document.
* **Contour Detection:** Algorithmically identifies the largest rectangular contour representing the document sheet.
* **Perspective Transformation:** Applies a mathematical warp perspective (Bird's-Eye View) to align and flatten the document, correcting image distortion and optimizing the data for OCR accuracy.

### 3. Data Extraction (OCR)
* **Text Recognition:** Deploys **PyTesseract** (Tesseract OCR engine) on the transformed, flattened image to extract embedded textual data with high accuracy.
* **Data Parsing:** Converts the visual text into structured string formats ready for database loading or further NLP processing.

## 🛠️ Key Technologies
* **Core Language:** Python
* **Computer Vision & Image Processing:** OpenCV (`cv2`)
* **Data Extraction:** PyTesseract (OCR Engine)
* **Numerical Computation & Transformation:** NumPy
* **Data Visualization:** Matplotlib (for pipeline stage monitoring)
