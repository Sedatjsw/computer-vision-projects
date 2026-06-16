# Multi-modal Document Understanding Pipeline

This project presents a document processing pipeline that combines Computer Vision and Natural Language Processing (NLP) techniques to analyse different types of real-world document images.

## Project Overview

The goal of this project is to explore how Computer Vision and NLP techniques can be integrated into a single pipeline for document understanding and information extraction.

The project focuses on building a complete end-to-end workflow rather than developing a highly optimised production system.

The pipeline was tested on multiple document types with different layouts and structures, including:

* Academic poster
* Booking confirmation form
* Financial documents (invoice and statement)
* Pharmacy receipt

Using different document categories helped evaluate how the same processing pipeline behaves across various document structures and image qualities.

---

## Pipeline Architecture

The system is designed as a multi-modal document analysis pipeline.

### Image Preprocessing (OpenCV)

* Grayscale conversion
* Thresholding techniques
* Noise reduction
* Adaptive preprocessing for difficult images

### OCR Text Extraction (Tesseract OCR)

* Extraction of raw text from document images
* Conversion of image-based documents into machine-readable text

### Text Preprocessing

* Text cleaning
* Tokenisation
* Stopword removal
* Lemmatisation

### Text Feature Extraction

* TF-IDF feature extraction
* Keyword and key phrase identification

### Named Entity Recognition (NER)

* Rule-based extraction of dates, monetary values, names, and phone numbers
* spaCy-based entity recognition for organisations, locations, people, and dates

### Document Classification

* Rule-based document categorisation using extracted textual and visual features

### Visual Feature Detection

* Contour detection
* Layout region analysis
* Detection of tables, forms, invoices, and receipt sections

### Image Segmentation

* Segmentation of documents into meaningful visual regions
* Grouping of text blocks and structured components

### Multi-modal Integration

* Combination of OCR results, visual analysis, document structure, and named entities into a unified pipeline

### Final Output

* Structured summary of extracted text, entities, visual regions, and document-level insights

---

## Key Observations

* OCR performance is strongly affected by image quality and document structure
* Image preprocessing significantly improves OCR quality for noisy documents
* Academic documents generate richer keyword extraction results due to larger text content
* Financial and receipt documents are more structured and numeric in nature
* TF-IDF performs less effectively on short structured documents
* Rule-based classification performs well for small datasets
* Complex layouts produce a higher number of detected visual regions

---

## Technologies Used

* Python
* OpenCV
* Tesseract OCR
* spaCy
* NLTK
* Scikit-learn
* Pandas
* Matplotlib

---

## Limitations

This project focuses on demonstrating the overall pipeline rather than optimising model performance.

Current limitations include:

* Small dataset size
* OCR inaccuracies affecting downstream NLP tasks
* Contour-based visual detection with limited precision
* Complex document layouts producing noisy segmentation outputs
* Named Entity Recognition sensitivity to OCR errors

---

## Conclusion

This project demonstrates how Computer Vision and NLP techniques can be combined into a unified pipeline for document understanding.

The integration of OCR, visual analysis, named entity recognition, and document structure analysis provides a strong foundation for multi-modal document processing systems.

The project also highlights practical challenges commonly encountered in real-world document analysis, including OCR quality, layout variability, and noisy visual structures.

---

## Technologies & Concepts Demonstrated

* Computer Vision
* OCR Processing
* NLP Pipelines
* Named Entity Recognition
* Image Segmentation
* Document Classification
* Multi-modal Data Processing
* Feature Extraction
* Python Data Processing Workflows

---

## Author

Sedat Aydin
MSc Big Data Analytics & Artificial Intelligence
