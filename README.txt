## Overview
A deep learning model for detecting oral diseases using custom CNN architecture. The model is trained to classify different types of oral diseases from images with data augmentation techniques and class weight balancing to handle imbalanced datasets.

## Features
- Custom CNN architecture optimized for oral disease detection
- Data augmentation for improved model generalization
- Class weight balancing for handling imbalanced datasets
- Learning rate scheduling with exponential decay
- Comprehensive evaluation metrics and visualizations
- Built with TensorFlow/Keras

## Project Structure
```
├── model/
│   └── oral_disease_custom_model.keras
├── data/
│   ├── train/
│   ├── valid/
│   └── test/
├── results/
│   ├── metrics_plot.png
│   ├── confusion_matrix.png
│   └── results.json
├── src/
│   └── train.py
├── requirements.txt
├── README.md
```

## Requirements
- TensorFlow >= 2.0
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Python = 3.12.7

## Installation
```bash
# Clone the repository
git clone https://github.com/Utkarsh251106/Oral-disease-detection.git
cd Oral-disease-detection

# Install dependencies
pip install -r requirements.txt
```

## Model Architecture
- Input Layer: 320x320x3
- Convolutional Layers:
  - Conv2D (32 filters) + BatchNorm + MaxPooling
  - Conv2D (64 filters) + BatchNorm + MaxPooling
  - Conv2D (128 filters) + BatchNorm + MaxPooling
- Dense Layers:
  - Flatten
  - Dense (128 units)
  - Dropout (0.3)
  - Output Dense Layer (number of classes)

## Training
- Batch Size: 32
- Image Size: 320x320
- Data Augmentation:
  - Random Horizontal Flip
  - Random Rotation (0.2)
  - Random Zoom (0.2)
  - Random Contrast (0.2)
- Learning Rate: Exponential decay (initial: 1e-4)
- Early Stopping with patience of 5 epochs

## Usage
1. Prepare your dataset in the following structure:
```
dataset/
├── train/
│   ├── class1/
│   ├── class2/
│   └── ...
├── valid/
│   ├── class1/
│   ├── class2/
│   └── ...
└── test/
    ├── class1/
    ├── class2/
    └── ...
```

2. Run the training script:
```bash
python src/train.py
```

## Results
The model generates:
- Classification metrics (precision, recall, F1-score)
- Confusion matrix
- Performance visualizations
- Saved model weights

## License
MIT License

## Contributors
- [Your Name]

## Citation
If you use this project in your research, please cite:
```
@misc{oral-disease-detection,
  author = {[Your Name]},
  title = {Oral Disease Detection Using Deep Learning},
  year = {2024},
  publisher = {GitHub},
  url = {https://github.com/Utkarsh251106/Oral-disease-detection}
}
```