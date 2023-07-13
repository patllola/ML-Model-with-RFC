# ML-Model-
Machine Learning Model For Incoming Data Prediction.

# Code Repository: Random Forest Classifier

This repository contains code for training and evaluating a Random Forest Classifier using the `scikit-learn` library. The classifier is trained on a dataset of healthy and unhealthy samples obtained from TDMS files.

## Installation

To run the code, you need to install the following dependencies:

- `numpy`: version 1.23.5
- `pandas`: version 1.3.5
- `scikit-learn`: version 1.0.1
- `nptdms`: version 1.7.0

You can install the dependencies using the following command:

```bash
pip install numpy pandas scikit-learn nptdms
```

## Usage

1. Clone the repository:
   ```bash
   git clone <repository_url>
   ```
   
2. Install the required dependencies as mentioned above.

3. Run the main script:
   ```bash
   python main.py
   ```

## Preprocessing

The preprocessing step involves reading TDMS files, extracting data from different channels, and combining them into a single DataFrame. The data is then cleaned by removing missing values and unnecessary columns. The target column is set as "Status," where 0 represents healthy samples and 1 represents unhealthy samples.

## Model Training

The script uses a Random Forest Classifier from the `scikit-learn` library to train the model. The hyperparameters, such as the number of estimators and the minimum number of samples per leaf, can be set via command-line arguments. The model is trained using the training dataset and evaluated using the testing dataset. The classification report, including precision, recall, and F1-score, is printed to assess the model's performance.

## Saving the Model

After training, the model is saved as a joblib file (`model.joblib`) in the specified output directory.

## Additional Information

Please note that the provided code assumes the availability of TDMS files in the specified file paths. You may need to modify the file paths or provide your own dataset accordingly.
