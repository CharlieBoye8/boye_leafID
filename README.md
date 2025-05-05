# Leafsnap Species Classification – DS 325 Final Project

This repository contains code and analysis for my final project in DS 325: Applied Data Science. The focus of this project is using the Leafsnap dataset to classify tree species from images of their leaves using machine learning methods.

## Project Files

- `EDA.ipynb`: Initial exploratory data analysis of the Leafsnap dataset.
- `LeafSnapKNN.ipynb`: Implementation of a K-Nearest Neighbors model.
- `Final Project.pdf`: Final written report summarizing methods and results.

## Dataset

The dataset used is the Leafsnap dataset, originally developed by researchers from Columbia University, University of Maryland, Smithsonian Institution, and others. The version used here was retrieved from Kaggle:  
https://www.kaggle.com/datasets/xhlulu/leafsnap-dataset

## Approach

This project explored both simple and deep learning-based classification methods:

- Started with basic data cleaning and visualization
- Applied a KNN model to a filtered dataset (top 10 species with most samples)
- Built and trained CNN models, including MobileNetV2 with transfer learning
- Switched from segmented grayscale images to full-color lab images for better performance

Key improvements were made after identifying issues with poor segmentation and image quality. Once the dataset was cleaned, MobileNetV2 was able to reach ~98% validation accuracy.

## Steps

1. Filter to 10 most common species from lab images
2. Remove poorly segmented or black images
3. Create train/test split
4. Preprocess with resizing, normalization, and augmentation
5. Train KNN and MobileNetV2 models
6. Evaluate results and generate plots

## Results

- KNN provided solid baseline performance.
- CNNs initially underperformed due to poor preprocessing.
- After switching to better image inputs, MobileNetV2 achieved high accuracy.
- The final model showed minimal overfitting and strong generalization on test data.

## Conclusion

This project demonstrated the importance of proper data cleaning and preprocessing, especially when working with image datasets. While deep learning models offer strong performance, simpler models like KNN are still very useful.

## References

- Kumar et al., 2012. *Leafsnap: A computer vision system for automatic plant species identification*. ECCV.
- https://www.kaggle.com/datasets/xhlulu/leafsnap-dataset
