
# Chest X-Ray Pneumonia Classification

## Project Overview

This project uses Deep Learning and Convolutional Neural Networks (CNNs) to classify chest X-ray images into two categories:

- **NORMAL**
- **PNEUMONIA**

The goal is to demonstrate how deep learning techniques can be applied to medical image classification using TensorFlow and Keras.

**Disclaimer:** This project is for educational purposes only. It is not a clinically validated diagnostic system and must not be used to make medical decisions.

## Dataset

The project uses the **Chest X-Ray Images (Pneumonia)** dataset.

The dataset contains chest X-ray images organized into two classes:

- NORMAL
- PNEUMONIA

The downloaded dataset is organized into:

```text
data/
└── chest_xray/
    ├── train/
    │   ├── NORMAL/
    │   └── PNEUMONIA/
    └── test/
        ├── NORMAL/
        └── PNEUMONIA/
```

The original training folder contains 4,718 images, while the test folder contains 624 images.

Since the downloaded version does not contain a separate validation folder, the training data is divided into:

- 80% training data (3,775 images).
- 20% validation data (943 images).

The test dataset is kept separate for final evaluation.

**Note:** The dataset is not included in this repository. Download it separately and place it in the directory structure shown above.

## Technologies and Libraries

- Python
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Pillow
- Jupyter Notebook

## Project Workflow

### 1. Exploratory Data Analysis
- Explore the dataset structure.
- Count images in each class.
- Visualize the class distribution.
- Display sample X-ray images.

### 2. Data Preprocessing
- Resize images to 150 × 150 pixels.
- Load images in RGB format.
- Normalize pixel values to the range 0–1.
- Split training data into training and validation subsets.

### 3. Data Augmentation
Apply random transformations to training images:
- Horizontal flipping.
- Random rotation.
- Random zoom.

### 4. Model Development
Build a CNN using:
- Convolutional layers.
- Max pooling layers.
- Flatten layer.
- Dense layer.
- Dropout.
- Sigmoid output layer.

### 5. Model Training
- Train the CNN using TensorFlow/Keras.
- Apply class weights to address class imbalance.
- Use Early Stopping.
- Save the best model using Model Checkpoint.

### 6. Model Evaluation
Evaluate the model on the separate test dataset using:
- Accuracy.
- Precision.
- Recall.
- F1-score.
- Classification report.
- Confusion matrix.

Training and validation accuracy/loss curves are also generated to analyze model performance.

## Repository Structure

```text
Chest_Xray_Pneumonia_Classification/
│
├── data/
│   └── chest_xray/
│       ├── train/
│       └── test/
│
├── models/
│   └── best_chest_xray_model.keras
│
├── outputs/
│   ├── accuracy_curve.png
│   ├── loss_curve.png
│   ├── confusion_matrix.png
│   ├── classification_report.txt
│   ├── training_history.csv
│   └── project_summary.csv
│
├── notebooks/
│   └── chest_xray_classification.ipynb
│
├── .gitignore
├── requirements.txt
└── README.md
```

The dataset, virtual environment, generated outputs, and trained model may be excluded from GitHub depending on their size and repository requirements.

## Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Engineer-ZainabTaleb/Chest_Xray_Pneumonia_Classification.git
```

```bash
cd Chest_Xray_Pneumonia_Classification
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

### 3. Activate the Environment

Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### 4. Install Dependencies

```bash
pip install -r requirements.txt
```

### 5. Download the Dataset

Download the Chest X-Ray Images (Pneumonia) dataset and place the `chest_xray` folder inside the `data` directory, following the structure described above.

### 6. Run the Notebook

Open the project in Jupyter Notebook or Visual Studio Code and run:

```text
notebooks/chest_xray_classification.ipynb
```

Run the notebook cells in order.

## Results

The model is evaluated using the test dataset.

The final results will be documented here after the final training run:

| Metric | Result |
|---|---|
| Accuracy | To be updated |
| Precision | To be updated |
| Recall | To be updated |
| F1-Score | To be updated |

The project also generates a classification report, confusion matrix, and training performance graphs.

## Future Improvements

- Experiment with transfer learning using MobileNetV2 or EfficientNet.
- Compare different CNN architectures.
- Experiment with different image sizes.
- Improve generalization using more diverse datasets.
- Evaluate the model on independent datasets.

## Author

Zainab Taleb

GitHub: [Engineer-ZainabTaleb](https://github.com/Engineer-ZainabTaleb)

LinkedIn: [Zainab Taleb](https://www.linkedin.com/in/zainab-taleb22/)

