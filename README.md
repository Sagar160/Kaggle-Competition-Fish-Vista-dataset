# Kaggle-Competition-Fish-Vista-dataset

# Dataset
![image](https://github.com/user-attachments/assets/c8e293e3-d12c-4da7-8e95-455bffa9e421)
Introducing Fish-Vista, a dataset of ~60K curated fish images across 419 species, designed for tasks like species classification, trait identification, and trait segmentation. Includes pixel-level annotations for 9 traits on 2427 images, enabling fine-grained analysis to advance biological discoveries with AI.

# Objective
Classify fish species from a highly imbalanced dataset, where ~80% of classes have fewer than 50 samples per class and only ~2% of classes have more than 1000 samples, using strategies to address class imbalance and improve generalization.

# Novel Technique: RANDOM DATA AUGMENTATION  

In this approach, we randomly select a subset of the training dataset at every epoch. The assumption is that we can reduce overfitting while allowing the model to train on the entire original dataset.

The strategy is implemented using two main steps:  

### Pre-processing  
We pre-process the data by applying basic transformations to all images (as mentioned above). However, pre-processing is implemented with a higher probability of random processing for classes with fewer images.  

### Data Selection Strategy  
We designed a data selection strategy for each epoch. For our case, we selected 3 images per class plus 2,000 random images for training and 3 images per class plus 400 random images for validation. 

For training purposes, the dataset was split into 90% training and 10% validation using a stratified splitting methodology.  

# Results
![image](https://github.com/user-attachments/assets/2d3c2a24-7328-43d7-ada0-e7585717ea03)

## Technologies and Tools
- Python
- Pandas, NumPy
- PyTorch
- Scikit-learn
- Vision Transformer
- Computer Vision
- Transfer Learning
