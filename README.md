# e6692_2026spring_Project_EFTJ_et2833

# Lichen Segmentation Project

## Project Overview

This project focuses on using DL models trained in PyTorch. The workflow includes dataset preparation, model training, human-in-the-loop (HITL) mask generation, evaluation, and deployment benchmarking on NVIDIA Jetson hardware.

# Repository Structure

## `collab_files/`
Contains all Collab notebooks and experiments used during dev. For example:

 `Round1_Training_Val_Models/`:  initial training and validation pipeline using annotations exported from CVAT
 `HITL_First_Run/`:  workflow used to generate masks for approximately 200 additional training image
`Training_HITL/`: retraining workflows using the expanded HITL dataset.

## Utils
These include:
`lichen_dataset.py`: Defines the custom PyTorch dataset class used for segmentation training.

`evaluate_segmentation`:evals segmentation models erformance against ground-truth masks.
`training`: raining pipeline saves the best-performing model weights based on validation loss.

## weight folders:

not uploaded to github, but containing saved model weights for their respective experiments and training runs.

# `On_Jetson/`

Contains deployment and benchmarking experiments performed on NVIDIA Jetson hardware.

# Workflow Summary

1. Annotate images in CVAT
2. Train initial segmentation models
3. Generate additional masks using HITL workflow
4. Retrain models on expanded dataset
5. Save optimized weights
6. Evaluate and benchmark models on Jetson hardware
