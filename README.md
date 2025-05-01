# Pet-Classification-Model

Pet Classification Using ResNet
Project Overview
This Python project implements a pet classification model using the ResNet (Residual Network) architecture to classify images of pets (e.g., cats, dogs) with high accuracy. Built with TensorFlow, the project leverages transfer learning on a pre-trained ResNet model, fine-tuned on a pet image dataset. It includes data preprocessing, model training, evaluation, and inference pipelines, making it suitable for applications like pet adoption platforms or veterinary tools.
Features

Dataset: Utilizes a labeled pet image dataset (e.g., Oxford-IIIT Pet Dataset) for training and testing.
Model: Employs ResNet (e.g., ResNet-50) pre-trained on ImageNet, fine-tuned for pet classification.
Preprocessing: Handles image resizing, normalization, and data augmentation (e.g., random flips, rotations).
Training: Supports customizable epochs, learning rate, and batch size with categorical cross-entropy loss and Adam optimizer.
Evaluation: Provides accuracy, precision, recall, and confusion matrix for model performance.
Inference: Allows classification of new pet images with a user-friendly script.

Requirements

Python 3.8+
TensorFlow 2.6+
NumPy
Pandas
Matplotlib
Scikit-learn
Pillow

Install dependencies using:
pip install -r requirements.txt

Project Structure
pet-classification-resnet/
├── data/                    # Dataset folder (e.g., Oxford-IIIT Pet Dataset)
├── models/                  # Saved trained models
├── src/
│   ├── data_preprocess.py   # Image preprocessing and data loading
│   ├── model.py             # ResNet model definition and fine-tuning
│   ├── train.py             # Training script
│   ├── evaluate.py          # Model evaluation and metrics
│   ├── inference.py         # Inference on new images
├── requirements.txt         # Project dependencies
├── README.md                # Project documentation
├── config.yaml              # Configuration file for hyperparameters

Getting Started

Clone the Repository:
git clone https://github.com/sruti-sreeya/Pet-Classification-Model.git
cd pet-classification-resnet


Prepare the Dataset:

Download the Oxford-IIIT Pet Dataset (or your preferred dataset).
Place it in the data/ folder and update config.yaml with the dataset path.


Install Dependencies:
pip install -r requirements.txt


Train the Model:
python src/train.py --config config.yaml


Evaluate the Model:
python src/evaluate.py --model models/resnet_pet.h5


Run Inference:
python src/inference.py --image path/to/pet_image.jpg



Configuration
Edit config.yaml to adjust:

Dataset path
Dataset : https://www.kaggle.com/datasets/tanlikesmath/the-oxfordiiit-pet-dataset
Model parameters (e.g., ResNet version, number of classes)
Training hyperparameters (e.g., epochs, learning rate, batch size)

Example config.yaml:
dataset:
  path: "data/oxford_pet"
  num_classes: 2
model:
  architecture: "resnet50"
  pretrained: true
training:
  epochs: 10
  batch_size: 32
  learning_rate: 0.001

Results

Training Accuracy: ~95% (varies by dataset and hyperparameters)
Test Accuracy: ~92%
Sample Output:Image: pet_image.jpg
Predicted Class: Dog (Confidence: 0.89)



Future Improvements

Add support for additional pet categories.
Implement model deployment using Flask or FastAPI.
Optimize for real-time inference on edge devices.
Integrate with a web interface for user interaction.

Contributing
Contributions are welcome! Please fork the repository, create a feature branch, and submit a pull request with your changes.
License
This project is licensed under the MIT License. See the LICENSE file for details.
Contact
For questions or feedback, reach out to [srutisreeya@gmail.com] or open an issue on GitHub.


