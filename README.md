# Crop Disease Prediction Using CNN

An AI-powered crop disease detection system that uses **Convolutional Neural Networks (CNN)** to identify diseases in tomato and cauliflower plants from leaf images and provide organic disease-management recommendations.

## Project Overview

Agriculture plays an important role in our daily lives, but crop diseases can significantly affect plant health and agricultural productivity.

This project uses Deep Learning and image classification techniques to detect diseases from plant leaf images. It analyses uploaded images, predicts the disease category, and provides recommendations to help manage the identified condition.

## Key Features

- **AI-Based Disease Detection:** Identifies diseases using CNN.
- **Multiple Crop Support:** Supports tomato and cauliflower plants.
- **Image Upload:** Upload leaf images for disease prediction.
- **Treatment Recommendations:** Provides organic disease-management suggestions.
- **Image Preprocessing:** Resizes and normalises images before prediction.
- **Data Augmentation:** Uses zoom, shear and horizontal flipping.
- **Model Evaluation:** Includes training, validation and testing.
- **Model Saving:** Saves and loads the trained TensorFlow model.

## Technologies Used

| Technology | Purpose |
|---|---|
| Python | Programming language |
| TensorFlow | Deep Learning framework |
| Keras | CNN model development |
| NumPy | Numerical operations |
| Pandas | Data handling |
| Matplotlib | Data visualisation |
| Seaborn | Visualisation |
| Scikit-learn | Dataset splitting and evaluation |
| Google Colab | Development environment |

## Supported Crops and Diseases

### Tomato
- Bacterial Spot
- Early Blight
- Late Blight
- Leaf Mold
- Septoria Leaf Spot
- Spider Mites
- Target Spot
- Tomato Yellow Leaf Curl Virus
- Tomato Mosaic Virus
- Healthy

### Cauliflower
- Bacterial Spot Rot
- Black Rot
- Downy Mildew
- Healthy

## CNN Model Architecture

The project uses a Convolutional Neural Network with the following architecture:

1. Convolutional Layer – 32 filters
2. Max Pooling Layer
3. Convolutional Layer – 64 filters
4. Max Pooling Layer
5. Convolutional Layer – 128 filters
6. Max Pooling Layer
7. Flatten Layer
8. Fully Connected Layer – 512 neurons
9. Dropout Layer – 0.5
10. Softmax Output Layer

### Model Configuration

- Image Size: 150 × 150
- Batch Size: 32
- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Activation: ReLU and Softmax
- Maximum Epochs: 15
- Early Stopping: Enabled

## Project Workflow

```text
       Dataset Collection
              |
              v
       Image Preprocessing
              |
              v
       Dataset Splitting
              |
              v
       Data Augmentation
              |
              v
        CNN Model Training
              |
              v
        Model Evaluation
              |
              v
        Model Saving
              |
              v
        Upload Leaf Image
              |
              v
       Disease Prediction
              |
              v
    Treatment Recommendations
```

## Dataset Structure

The project uses separate datasets for tomato and cauliflower.

```text
Mini project final/
│
├── Tomato/
│   ├── Bacterial Spot/
│   ├── Early Blight/
│   └── ...
│
└── Cauliflower/
    ├── Black Rot/
    ├── Downy Mildew/
    └── ...
```

The dataset is divided into:

- 70% Training
- 15% Validation
- 15% Testing

**Note:** The dataset is not included in this repository.

## Installation

Install the required libraries:

```bash
pip install tensorflow numpy matplotlib pandas scikit-learn seaborn tabulate ipywidgets
```

## Running the Project

This project was originally developed using Google Colab.

1. Open Google Colab.
2. Upload the project notebook.
3. Connect your Google Drive.
4. Place the tomato and cauliflower datasets in the required folders.
5. Update dataset paths if necessary.
6. Execute the notebook cells.
7. Train the CNN model.
8. Upload a leaf image to test disease prediction.

**Note:** The current Python file contains Google Colab-specific commands and Google Drive paths. It requires modification before running directly as a standalone local Python application.

## Future Enhancements

- Develop a user-friendly web application.
- Integrate real-time disease detection.
- Support additional crop varieties.
- Improve prediction accuracy.
- Add multilingual recommendations.
- Deploy the model as an online application.

## Author

**Abhiram PS**

GitHub: [Abhiram062004](https://github.com/Abhiram062004)

---

*This project was developed as a Deep Learning-based crop disease detection system to explore the application of Artificial Intelligence in agriculture.*
