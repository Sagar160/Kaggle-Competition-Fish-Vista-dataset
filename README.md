# Kaggle-Competition-Fish-Vista-dataset

# Dataset
![image](https://github.com/user-attachments/assets/c8e293e3-d12c-4da7-8e95-455bffa9e421)
Introducing Fish-Vista, a dataset of ~60K curated fish images across 419 species, designed for tasks like species classification, trait identification, and trait segmentation. Includes pixel-level annotations for 9 traits on 2427 images, enabling fine-grained analysis to advance biological discoveries with AI.

# Objective
Classify fish species from a highly imbalanced dataset, where ~80% of classes have fewer than 50 samples per class and only ~2% of classes have more than 1000 samples, using strategies to address class imbalance and improve generalization.

# Novel Techniue: RANDOM DATA AUGMENTATION
Within this approach we are randomly selecting a subset of the training dataset at every epoch. The assumption is that we can reduce overfitting, while allowing the model to still train on the entire original dataset.

The strategy is implemented using two main steps:
Pre-processing: Where we pre-process the data by applying some basic transformations to all images(mentioned above). However, pre-prcoessing is implmented with a higher probality of random processing for classes with few images.
Data selection strategy: Here we have designed a data selection startegy for each epoch. For our case, we selected 3 image per class plus 2000 random images for training and 3 image per class plus 400 random images for validation.

For training purposes the dataset was split into 90% training and 10% validation using a stratified splitting methodology (explained above).

# Results
![image](https://github.com/user-attachments/assets/2d3c2a24-7328-43d7-ada0-e7585717ea03)


