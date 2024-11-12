# Breast Histopathology Image Analysis

This project involves the analysis of breast histopathology images to detect invasive ductal carcinoma (IDC) from image patches. The dataset consists of histopathological image patches, where each patch is labeled as either containing IDC (class 1) or not (class 0). The goal of the project is to explore the dataset, analyze the images, and set up a machine learning pipeline to classify the patches into IDC vs. non-IDC.

## Project Overview

The dataset includes multiple histopathology image patches obtained from tissue samples of patients diagnosed with breast cancer. Each patient's dataset is contained within a folder, and each folder is divided into two subfolders representing the classes:
- `0`: Non-IDC (no cancerous tissue)
- `1`: IDC (invasive ductal carcinoma)

We perform exploratory data analysis (EDA), visualize the distribution of IDC vs. non-IDC patches, and build machine learning models for classification.

### Key Steps Involved
1. **Exploratory Data Analysis (EDA)**: 
   - Analyzing the distribution of patches per patient.
   - Visualizing healthy and cancerous tissue patches.
   - Investigating the class imbalance between IDC and non-IDC patches.

2. **Data Preparation**:
   - Storing the image paths, targets (labels), and patient IDs in a dataframe.
   - Reconstructing the breast tissue using image coordinates for each patient.

3. **Model Development**:
   - Setting up a machine learning pipeline to classify the image patches into IDC and non-IDC categories.
   - Applying strategies to address class imbalance and optimize the model performance.

4. **Visualization**:
   - Visualizing breast tissue slices and identifying cancerous patches.
   - Comparing tissue samples with and without cancer.

5. **Validation Strategy**:
   - Splitting the dataset into training and testing data to ensure the model generalizes well.
   
---

## Data Description

### Dataset
- The dataset consists of histopathological image patches.
- Each patient’s data is located in separate folders. The folder names represent patient IDs.
- Inside each patient folder, there are two subfolders:
  - `0`: Non-IDC (healthy tissue).
  - `1`: IDC (cancerous tissue).

The images are patch-based slices from breast tissue samples, where each patch is labeled as either 0 (non-cancerous) or 1 (cancerous).

### File Format
- The images are stored in `.jpg` or `.png` format.
- The dataset is divided by patient ID, with each image patch named according to its `(x, y)` coordinates within the tissue slice.

---

## Insights and Future Work

### Insights:
- The distribution of patches per patient is highly variable, with some patients having more than 80% IDC patches.
- The tissue slices have regions with varying concentrations of cancer, and the task involves distinguishing between healthy and cancerous tissue based on image patches.
- The classes are imbalanced, with more non-IDC patches than IDC patches. Techniques such as class weighting or oversampling may be applied to handle this imbalance.

### Future Work:
- Experiment with different deep learning models (e.g., CNN, ResNet) to improve classification accuracy.
- Investigate the possibility of using more advanced techniques like transfer learning to leverage pre-trained models.
- Address class imbalance using data augmentation, SMOTE, or other sampling techniques.
- Explore the integration of additional clinical data, such as patient history, to improve classification.
