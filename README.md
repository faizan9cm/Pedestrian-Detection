# Assignment Report: Pedestrian Detection Using DINO-4scale Model

## Objective
The goal of this assignment was to implement the DINO-4scale model with a ResNet-50 backbone for detecting pedestrians in a dataset consisting of 200 images collected within the IIT Delhi campus. The dataset was annotated in COCO format, providing a structured approach for training and evaluating the model.

## Dataset Overview
- **Total Images**: 200
- **Dataset Structure**: COCO format with images and annotations.
- **Train/Validation Split**: 
  - Training Set: 160 images
  - Validation Set: 40 images

## Methodology
1. **Environment Setup**:
   - Cloned the official DINO repository from GitHub.
   - Installed necessary dependencies and set up the environment.

2. **Training**:
   - Utilized the pre-trained DINO-4scale model to fine-tune on the pedestrian dataset.

3. **Evaluation**:
   - Ran the evaluation script to compute performance metrics on the validation set.

## Evaluation Metrics
- **Average Precision (AP)**:
  - AP@[ IoU=0.50:0.95 | area=all | maxDets=100 ]: **0.496**
  - AP@[ IoU=0.50 | area=all | maxDets=100 ]: **0.832**
  - AP@[ IoU=0.75 | area=all | maxDets=100 ]: **0.534**
  - AP@[ IoU=0.50:0.95 | area=small | maxDets=100 ]: **0.394**
  - AP@[ IoU=0.50:0.95 | area=medium | maxDets=100 ]: **0.633**
  - AP@[ IoU=0.50:0.95 | area=large | maxDets=100 ]: **0.718**

- **Average Recall (AR)**:
  - AR@[ IoU=0.50:0.95 | area=all | maxDets=1 ]: **0.099**
  - AR@[ IoU=0.50:0.95 | area=all | maxDets=10 ]: **0.471**
  - AR@[ IoU=0.50:0.95 | area=all | maxDets=100 ]: **0.595**
  - AR@[ IoU=0.50:0.95 | area=small | maxDets=100 ]: **0.514**
  - AR@[ IoU=0.50:0.95 | area=medium | maxDets=100 ]: **0.717**
  - AR@[ IoU=0.50:0.95 | area=large | maxDets=100 ]: **0.805**

## Results Analysis
- The model demonstrated strong performance, particularly at the lower IoU threshold (0.50), with an AP of **0.832** for all object sizes.
- Performance for larger objects was notably better, while small objects showed lower AP scores, indicating a potential area for improvement.
