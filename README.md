# Face Mask Detection Project

This project involves building a Convolutional Neural Network (CNN) to classify images as either showing a person wearing a mask or not wearing a mask. It was developed using Python and various machine learning and image processing libraries. Below is a breakdown of the project:

### 1. **Dataset Preparation**
- **Data Source**: The dataset is downloaded from Kaggle, containing images of people with and without masks.
- **Data Organization**: The dataset is split into two main folders: `with_mask` and `without_mask`, containing labeled images.

### 2. **Data Preprocessing**
- **Loading and Resizing Images**: Images are loaded using `PIL` and resized to 128x128 pixels.
- **Labeling**: Images from the `with_mask` folder are labeled `1`, and images from the `without_mask` folder are labeled `0`.
- **Normalization**: Image data is normalized by dividing pixel values by 255 to scale them between 0 and 1.

### 3. **Splitting Data**
- The dataset is split into training and testing sets using `train_test_split` from `sklearn` with an 80-20 ratio.

### 4. **Model Architecture**
- **Layers**:
  - `Conv2D` and `MaxPooling2D` for feature extraction.
  - `Flatten` for converting 2D data to 1D.
  - `Dense` layers with `ReLU` activation and `Dropout` for regularization.
  - Final `Dense` layer with `sigmoid` activation for binary classification.
- **Compilation**:
  - Optimizer: `Adam`
  - Loss function: `sparse_categorical_crossentropy`
  - Metrics: `accuracy`

### 5. **Training the Model**
- The model is trained for 5 epochs with an 80-20 validation split.
- Training metrics (accuracy and loss) are tracked and displayed.

### 6. **Evaluation**
- The model achieves an accuracy of ~90.5% on the test data.
- **Plotting**: Training and validation loss/accuracy are plotted to visualize model performance.

### 7. **Image Prediction**
- Users can input an image path for prediction.
- The input image is read using `cv2`, resized, normalized, and reshaped before being passed to the model for prediction.
- The model outputs whether the person in the image is wearing a mask or not.

### 8. **Libraries Used**
- `numpy`, `matplotlib`, `PIL`, `cv2`, `tensorflow`, `sklearn`

### 9. **Sample Result**
- Training accuracy: ~89.2%
- Validation accuracy: ~91.8%
- Test accuracy: ~90.5%

### 10. **Visualization**
- Training and validation loss/accuracy curves are plotted for better insights.

This project serves as a practical implementation for learning about CNNs in computer vision and image classification tasks.
