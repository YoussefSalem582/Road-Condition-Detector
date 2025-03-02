# RoadConditionDetector 🚧🛣️

A machine learning project to detect potholes and classify road conditions using a Decision Tree model.

![Road Condition Example](https://via.placeholder.com/600x400?text=Pothole+vs+Smooth+Road) *Example images*

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [Dataset](#dataset)
- [Model Training](#model-training)
- [Results](#results)
- [Contributing](#contributing)

## Overview
This project aims to automate road condition detection by classifying images into "pothole" or "smooth road" categories. It uses a Decision Tree classifier and image processing techniques to achieve this task. The workflow includes:
- Image collection from Bing.
- Preprocessing and feature extraction.
- Model training and evaluation.

## Features
- **Image Downloader**: Fetches pothole and smooth road images using Bing API.
- **OpenCV Integration**: Processes images for model compatibility.
- **Decision Tree Model**: Trains a classifier to predict road conditions.
- **Evaluation Metrics**: Generates accuracy scores, confusion matrices, and classification reports.

## Installation
1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/RoadConditionDetector.git
   cd RoadConditionDetector
   ```

2. **Install dependencies**:
   ```bash
   pip install bing-image-downloader opencv-python numpy scikit-learn joblib matplotlib seaborn
   ```

## Usage
1. **Download Images**:
   - Run the Jupyter notebook `ML_Project_Final (1).ipynb`.
   - Use the `download_images()` function to fetch datasets:
     ```python
     download_images("street potholes on roads", limit=100, output_directory="pothole_images")
     download_images("smooth well-maintained roads", limit=100, output_directory="no_pothole_images")
     ```

2. **Validate and Preprocess Images**:
   - The notebook includes a `validate_images()` function to remove corrupted files.

3. **Train the Model**:
   - The notebook script extracts features, splits data into train/test sets, and trains the Decision Tree.

4. **Evaluate Performance**:
   - Accuracy scores, confusion matrices, and classification reports are generated automatically.

## Dataset
- **Pothole Images**: 100+ images of roads with potholes.
- **Smooth Roads**: 100+ images of well-maintained roads.
- Images are resized and normalized for model input.

## Model Training
- **Feature Extraction**: Images are flattened into pixel arrays.
- **Decision Tree**: Configured with default hyperparameters (customizable in the notebook).
- **Evaluation**: Metrics include:
  - Accuracy
  - Precision/Recall
  - Confusion Matrix Visualization

## Results
After training, the model achieves:
- **Accuracy**: ~85% (example; run the notebook for actual results).
- **Confusion Matrix**: Visualized using Seaborn/Matplotlib.

![Confusion Matrix](https://via.placeholder.com/400x300?text=Confusion+Matrix)  
*Example visualization*

## Contributing
Contributions are welcome! Open an issue or submit a PR for:
- Enhancing model performance (e.g., using CNNs).
- Expanding the dataset.
- Improving documentation.
