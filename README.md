# Image-text-segmentation-OCRs-
Implementation of an Optical Character Recognition (OCR) system designed with classical image processing and Convolutional Neural Networks (CNNs). An university project for the _Proyecto Para Ciencia de Datos"_ subject.


## Abstract
In this document, a comprehensive implementation of an Optical Character Recognition (OCR) system designed from scratch will be presented, we will emphasise in the segmentation process for the precise extraction of text from images. Multiple strategies and approaches will be addressed to solve this challenge, highlighting the advantages of segmentation compared to other commonly used techniques. The methodology used involves segmenting each letter in the image and then classifying it with the assistance of a Deep Learning model. An evaluation of the results obtained through the proposed implemen- tation will be provided, comparing them with state of the art OCR models. The effectiveness of the proposed implementation was assessed using quantitative metrics, including the accuracy rate in letter identification. The strengths and limitations of the proposed implementation will be carefully examined, em- phasizing the areas where it matches existing models and those where improvements may be needed. This study aims to create a baseline model for OCR implementation that can serve as a starting point for future improvements in both performance and calculation speed.

Although the results obtained are not bad with an aver- age accuracy of 84%, it is still behind the state of the art models. Current ViT models are able to reach an average of 93%, while also allowing a wide variety of images used as input and still get reasonable results. Our model may be quick to train compared to the training times of a Transformer, but it is still not able to generalize to different kind of images and only accepts pdf style documents of a certain kind. Changing the words size in the document or introducing other fonts that are not com- monly used may decrease significantly the quality of the results.

## Usage (datasets)

The datasets used for training CNN models in this project can be found in *Kaggle*, they are the "EMNIST" and "Digital Letters" datasets:

- EMNIST: https://www.kaggle.com/datasets/crawford/emnist
- Digital Letters: https://www.kaggle.com/datasets/adamkaniasty/digital-letters?select=digital_letters.csv

## Usage (Notebooks)

There are two Jupyter notebooks that can be found in the _"Notebooks"_ folder:

- OCR limpieza entrenamiento.ipynb: whith the classification model and the preprocessing process
- OCR segmentacion prediccion.ipynb: which contains the segmentation process

It is highly recommended to save the CNN model once it's trained. So the notebook _"OCR limpieza entrenamiento.ipynb"_ does not need to be executed again from scratch, so a functional pretrained CNN only needs to be loaded into the "OCR segmentacion prediccion.ipynb" notebook. Due to file sizes, we have not been able to upload our pretrained model into this repository.

## Data (examples used)

The data we used to test the model is in the _"Data"_ folder, there are two type of images, the ones labeled as _"historiaX"_ that is a story made up by chatgpt, recreating a pdf style document, and images labeled as _"EjemploX"_, examples taken from internet. All images sources will be referenced in the PCD paper.

## OCR paper

There is a file _"OCR paper"_ located in the main branch which has an in depth explanation of the project, where all subjects regarding preprocessing, obtaining data, models training and results will be covered, including comparisons with state of the art models and both its advantages and disadvantages.
