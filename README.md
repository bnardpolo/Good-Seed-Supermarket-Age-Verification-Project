# Good-Seed-Supermarket-Age-Verification-Project
Good Seed Supermarket Age Verification Project  (Computer Vision)
# Good Seed Supermarket Age Verification Project

## Project Overview

The Good Seed supermarket chain aims to leverage Data Science to ensure compliance with alcohol laws, particularly in preventing the sale of alcohol to underage individuals. The project focuses on utilizing computer vision methods to determine a person's age from photographs taken at the checkout area, where cameras are triggered when alcohol is being purchased.

## Project Objectives

The primary objective is to build and evaluate a model for verifying the age of individuals using images captured by checkout area cameras. Key considerations include variations in age, race, and potential challenges such as incomplete images, presence of objects in the background, and varying lighting conditions.

## Dataset

The dataset consists of photographs of individuals with their ages annotated. The images capture diverse age groups, ranging from young children to senior citizens. Notably, the images are cropped and may not display the full body. Additionally, some images contain objects in the background, and there may be variations in lighting across the dataset.

## Findings

Upon initial evaluation of the dataset, it was observed that:

- The dataset includes individuals of various races and ages, including those under 10 and senior citizens.
- Images are cropped and do not display the full length of individuals.
- Some images feature objects in the background.
- Lighting conditions vary across the dataset.

## Model Training

The model training involved several iterations, each with adjustments to parameters and architecture. The key training details are as follows:

- **Epochs:** 5
- **Batch Size:** 16
- **Learning Rate:** Varied across iterations
- **Model Architecture:** Adjusted by removing the zooming operation and Dense layer of 128 neurons in later iterations.


## Conclusions

1. The initial model with a batch_size of 32 and learning_rate of 0.01 yielded a MAE of approximately 18 years.
2. Lowering the learning_rate to 0.00002 resulted in a worse performance, with the MAE decreasing to 9 years.
3. Fine-tuning the model by removing the zooming operation, reducing the batch_size to 16, and removing the Dense layer of 128 neurons, and training for 5 epochs, improved the MAE to 7.1 years.
4. Further enhancements could be achieved by incorporating dropout and increasing the training time.
