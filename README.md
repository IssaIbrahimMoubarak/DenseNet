

# Plant Leaf Classification using DenseNet

## Project Overview 🌱

This project focuses on building a deep learning model for the classification of plant leaf images, specifically for tomato leaves. The model architecture is based on the DenseNet framework, which is known for its efficient and effective use of parameters through dense connections. The code reads, preprocesses, and normalizes image data before training a DenseNet model for classification.

## Table of Contents 📑

- [Project Overview](#project-overview-🌱)
- [Installation](#installation-🛠️)
- [Data Preprocessing](#data-preprocessing-🖼️)
- [Model Architecture](#model-architecture-🏗️)
- [Training](#training-🏋️)
- [Results](#results-📊)
- [Contributors](#contributors-🤝)

## Installation 🛠️

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/username/plant-leaf-classification.git
   cd plant-leaf-classification
   ```
2. **Install Dependencies**:
   Ensure you have Python installed (preferably 3.7 or later). Then install the required packages:

   ```bash
   pip install -r requirements.txt
   ```
3. **Directory Structure**:
   Ensure your directory structure for the images is as follows:

   ```
   /Data
   ├── TrainData
   │   ├── Class1
   │   ├── Class2
   │   └── ...
   └── TestData
       ├── Class1
       ├── Class2
       └── ...
   ```

## Data Preprocessing 🖼️

- **Loading Images**:
  The script uses `os.walk` to traverse the dataset directory, loading images from each class subfolder. The images are resized to 100x100 pixels for uniformity.
- **Normalization**:
  Images are normalized to have a mean of 0 and a standard deviation of 1 to stabilize the learning process.
- **Visualization**:
  Use the provided function `plot_images` to visualize sample images from the dataset.

## Model Architecture 🏗️

The model is built using the DenseNet architecture:

- **Dense Blocks**: Consist of multiple layers where each layer receives input from all previous layers.
- **Transition Layers**: Reduce the size of feature maps using convolution and pooling.
- **Global Average Pooling**: Reduces each feature map to a single value, preventing overfitting and reducing parameters.

The model is compiled using the Adam optimizer with categorical crossentropy as the loss function, optimized for multi-class classification.

## Training 🏋️

The model is trained for 50 epochs with a batch size of 64:

- **Training Data**: The preprocessed and normalized images are fed into the model.
- **Saving the Model**: After training, the model is saved as `DenseNet_groupe_2.h5`.

To train the model, simply run the script:

```bash
python train_model.py
```

## Results 📊

Upon completion of the training, the model’s performance is evaluated based on the accuracy metric. The final trained model is saved for future predictions or evaluations.

## Contributors 🤝

This project was developed by:

- **ISSA IBRAHIM Moubarak**
