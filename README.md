Crop Disease Prediction Using CNN
An image-based crop disease classification project built with Python, TensorFlow/Keras, and Convolutional Neural Networks (CNNs). The model is designed to classify leaf images from tomato and cauliflower plants and display disease-management recommendations associated with the predicted class.
Project status: The uploaded Python file was exported from Google Colab. It currently contains Colab-specific commands, Google Drive paths, and experimental notebook cells. The project is therefore best treated as a Colab-based prototype until those parts are cleaned up for standalone local execution.

Features
- Image classification for tomato and cauliflower leaf conditions.
- CNN model built with TensorFlow/Keras.
- Image resizing to 150 × 150 pixels and pixel rescaling.
- Training-time data augmentation: shear, zoom, and horizontal flip.
- Training, validation, and test dataset split.
- Early stopping based on validation loss.
- Prediction output for an uploaded leaf image.
- Text-based recommendations mapped to supported disease classes.
- Model saving and loading using Keras.
Technologies Used
- Python
- TensorFlow / Keras
- NumPy
- Matplotlib
- scikit-learn
- Pandas
- Seaborn
- ipywidgets
- tabulate
Supported Classes
The class labels in the prediction section of the current code include:

Cauliflower
- Bacterial spot rot
- Black Rot
- Downy Mildew
- Healthy
Tomato
- Bacterial spot
- Early blight
- Late blight
- Leaf Mold
- Septoria leaf spot
- Spider mites (Two-spotted spider mite)
- Target Spot
- Tomato Yellow Leaf Curl Virus
- Tomato mosaic virus
- Healthy
The code includes recommendation text for these labels. Recommendations are general project guidance and should be checked against local agricultural advice before being used to treat crops.
Model Architecture
The main training model in the script uses the following sequence:
1. Conv2D — 32 filters, 3 × 3 kernel, ReLU
2. MaxPooling2D — 2 × 2
3. Conv2D — 64 filters, 3 × 3 kernel, ReLU
4. MaxPooling2D — 2 × 2
5. Conv2D — 128 filters, 3 × 3 kernel, ReLU
6. MaxPooling2D — 2 × 2
7. Flatten
8. Dense — 512 units, ReLU
9. Dropout — 0.5
10. Dense output layer — softmax, sized to the training generator's number of classes
Compilation settings in the script
- Optimizer: Adam
- Loss: categorical cross-entropy
- Metric: accuracy
- Maximum epochs: 15
- Batch size: 32
- Early stopping: monitors val_loss, patience 5, restores best weights
Workflow
Tomato + Cauliflower image folders
              |
              v
       Split into train,
     validation, and test
              |
              v
       Image preprocessing
      and augmentation
              |
              v
        Train CNN model
              |
              v
       Evaluate the model
              |
              v
         Save the model
              |
              v
     Upload a leaf image
              |
              v
       Predict the class
              |
              v
   Display mapped recommendations
Dataset Organisation
The script expects the original dataset to be arranged in class-specific folders. The folder names become the class labels.

Example structure:
Mini project final/
├── Tomato/
│   ├── Tomato___Bacterial_spot/
│   ├── Tomato___Early_blight/
│   └── ...
└── Cauliflower/
    ├── Cauliflower - Bacterial spot rot/
    ├── Cauliflower - Black Rot/
    └── ...
The script creates a split directory with this structure:
split_dataset/
├── train/
│   ├── <class_name>/
│   └── ...
├── validation/
│   ├── <class_name>/
│   └── ...
└── test/
    ├── <class_name>/
    └── ...
The split ratios configured in the script are 70% training, 15% validation, and 15% testing.

Dataset note: The dataset itself is not included in this repository. Add the dataset source and licence here if you have permission to share that information. Do not upload datasets unless their terms allow redistribution.
Running the Current Project in Google Colab
1. Open the Python file in Google Colab, or upload the notebook version of the project.
2. Upload or place the tomato and cauliflower datasets in your Google Drive using the folder names expected by the script.
3. Update the dataset paths in the code if your Google Drive folder structure is different.
4. Run the notebook cells in order.
5. Train the model and review the evaluation output.
6. Upload a leaf image in the notebook widget to test prediction.
The current script uses Google Drive paths under /content/drive/MyDrive/Mini project final/ and includes !pip install commands, so it will not run unchanged as a normal local Python script.
Installation Requirements
Install the listed Python packages in your environment:
pip install -r requirements.txt
For the current Colab workflow, Google Colab provides many of these packages already. The notebook also mounts Google Drive to access the dataset and saved model.
Repository Structure
Crop-Disease-Prediction/
├── mini_final_project.py
├── requirements.txt
├── README.md
├── .gitignore
└── assets/
    └── screenshots/
Screenshots
Add genuine screenshots from your own project to assets/screenshots/, then replace the placeholders below with the image filenames.
<!-- Example:
![Leaf image upload interface](assets/screenshots/image-upload.png)
![Prediction and recommendation output](assets/screenshots/prediction-result.png)
![Model training output](assets/screenshots/training-output.png)
-->- Leaf image upload interface
- Predicted disease result and recommendation
- Model training or evaluation output
Important Notes / Current Limitations
- The code contains Google Colab-specific commands and Google Drive paths.
- The script includes repeated image-upload widget code.
- A later experimental section creates a separate model with a three-class output, while the main prediction code defines fourteen class labels. Review or remove this experimental section before presenting final model metrics.
- The classification-report section currently generates random example labels (y_true and y_pred), not predictions from the actual test dataset. Do not use those values as real model performance results.
- The project should be refactored and tested before claiming that it runs as a standalone local application.
Future Improvements
- Refactor the notebook into reusable Python modules.
- Replace fixed Google Drive paths with configurable local paths.
- Add a clean web interface using Flask or Streamlit.
- Generate evaluation reports from actual test-set predictions.
- Add confusion matrix and per-class precision, recall, and F1-score using real predictions.
- Add model confidence scores and clearer user guidance.
Author
Abhiram PS

GitHub: Abhiram062004

If you use or build upon this project, please verify dataset licensing and validate disease-management recommendations with a qualified agricultural source.