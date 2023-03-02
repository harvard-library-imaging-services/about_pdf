---
title: "About PDFs"
author: "bill comstock"
date: "02 March, 2023"
output:
  slidy_presentation: 
    incremental: yes
    keep_md: yes
    css: styles.css
  ioslides_presentation: 
    incremental: yes
    keep_md: yes
---



## Four flavors of PDF

* "True", digitally created PDF
* "Image only" PDF
* Searchable, image-based PDF
* Hybrid (image & character description) PDF

## True, perfect PDFs

Given a choice, this is the PDF you want.<br /><br />

The text is encoded descriptively: This font, at this size, should be rendered in this specific location on the page, or *canvas*. The font is described as a shape and can be scaled to any size output without degradation.

Because each character is explicitly defined by font, searches are run against a perfect index.


## "Image only" PDFs

These PDFs are so different from *true*, *perfect* PDFs, I wish they were called something else.

An *image only* PDF is just a sequence of raster images--grids of color and tone values.

## "Image only" PDFs, shortcomings

* These PDFs may have images of text, but the text cannot be searched. The PDF is only a sequence of images--grids of color and tone values.

* These files are frequently too large to open and navigate easily. 

## Searchable, image-based PDFs

These PDFs are also a sequence of images, but there is, typically, an imperfect index available for searching. The index is produced by OCR software that works to identify characters and words by analyzing the page-images.

## Searchable, image-based PDFs, shortcomings

* Like *image only* PDFs, these files are often too large for users to open and navigate easily.

* The OCR used to identify page-image text, typically, has errors. Pages typeset before computers, discolored pages, pages with schmutz, marginalia, or elaborate layouts--all of these characteristics degrade OCR accuracy, often dramatically.


## Hybrid (image & character description) PDF

Image-based PDFs with OCR-generated text can be converted to a hybrid of *true, perfect* and *image based*. The software will look for OCR-generated text that the software has assigned a high confidence score, indicating it has likely identified the fonts and characters correctly, and it will throw away the page-image source and replace the image data with a described font and layout.

A single hybrid page may include encoded text that replaces part of the image, and page-image fragments for zones where the OCR confidence scores are low.

## Hybrid PDF, shortcomings

* This technique reduces the PDF size (by replacing fat image data with lean character descriptions), but it is unreliable and can make some of the ugliest PDFs you'll ever see.

* Because the software discards image data that it replaces with character descriptions, you cannot recover from errors without access to the originally scanned page-images.

* Many fonts are licensed, so if Adobe cannot substitute a recognized character with the correct font, Adobe will substitute another that approximates the original.

## How does one create a *true, perfect* PDF from a scanned text?

Re-key the text using at least three typists and compare the three results to identify and recover from data-entry errors.


## How does one create an image-based PDF with a perfect index for searching?

OCR the pages and use special software to review potential errors and correct each one manually.

## What kind of PDFs does Imaging Services make?

Assuming a volume has text, and assuming Imaging Services has OCR software capable of identifying the language, and character set, Imaging Services creates image-based PDFs with an imperfect text index for searching.

## *Fin*

* [https://harvard-library-imaging-services.github.io/about_pdf/](https://harvard-library-imaging-services.github.io/about_pdf/)
* [Presentaton source file](aboutPDFs.Rmd)


