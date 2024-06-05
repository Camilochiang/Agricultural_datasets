# Goal
This folder contain mainly two important things:
1. Different datasets for object detection or instance segmentation collected along either the internet or at Agroscope (Conthey)
2. The tools for processing this data

# Annotation:
Each picture should have his own csv/txt file with the same name.

# Structure:
As Agroscope is planning to use this data for image analysis in intensive agriculture, the datasets were organized by class. This is as normaly only one class will be present and multiple models will be used (one for each class). There is no point of looking for carrots in apples trees.

The following structure is used:
Datasets
|- classes
    |- class_1
        |- raw: contain raw images if this ones were preprocessed 
        |- test: 
            |-images
            |-labels
            |-other_annotations: contain annotations in different formats other than the last used
        |- train
            |-images
            |-labels
            |-other_annotations: contain annotations in different formats other than the last used
        |- val:
            |-images
            |-labels
            |-other_annotations: contain annotations in different formats other than the last used        
        |- README.md: Contain detains about the class. PLEASE READ BEFORE CHANGING
    |- class_2
    ...
|- datasets_info
    |- dataset_1 : contain masks or other files already present in the dataset (e.g.: licences, masks, etc)
    ...
|- Tools : contain tools used for image preparation and labels transformation
|- datasets.json : details abouts each dataset
|- README.md : This file


# Datasets:
Different datasets were obtained. All pictures were renamed for later identification, using the following structure:
    NEW_NAME = XX_OLD_NAME
    where XX correspond to two capital letters that identify the dataset.

Several datasets were used. for details check the file `datasets.json`

# Tools:
Diferent tools were generated for this work and this specfic structrure. Check folder `Tools`

# New datasets:
You are free to add new datasets. but please keep the same structure and add the entry to `datasets.json`

# README.md review
20211203 - Camilo Chiang

# 20230706
Althought rgbd is not 2D, the color part can be used for rgb, so I decided to have them here.
So far i know
- one in apple
- one in tomatoes
- one in brocoli 