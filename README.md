# AI-Miscellaneous-Scripts

A collection of miscellaneous scripts for various AI-related tasks, including image classification, text classification, OCR, and web scraping.

## Files and Descriptions

### `data/`

- **Folder containing datasets** used by the scripts. Ensure to place your data files here before running the scripts.

### `DogVsCat.py`

This script is designed for binary image classification of dog and cat images. It performs the following tasks:

1. **Data Labeling**: Extracts labels from image filenames (e.g., `dog.1.jpg` or `cat.2.jpg`).
2. **Training Data Creation**: Processes and resizes images for training, and creates labels.
3. **Test Data Processing**: Prepares test data by resizing images and saving them to a `.npy` file.
4. **Model Training**: Uses a Convolutional Neural Network (CNN) implemented with TFLearn to classify images into 'dog' or 'cat'.

**Usage:**
1. Modify `TRAIN_DIR` and `TEST_DIR` to point to your directories with training and test images.
2. Run the script to train and evaluate the model:

    ```bash
    python DogVsCat.py
    ```

### `Short_Text_NN.py`

This script classifies short text headlines into different categories using a neural network. It includes the following steps:

1. **Data Preparation**: Loads a JSON dataset with news headlines and their categories.
2. **Text Preprocessing**: Converts text headlines into sequences and pads them to a uniform length.
3. **Model Definition**: Defines and compiles a neural network model with embedding and dense layers using TensorFlow/Keras.
4. **Training and Evaluation**: Trains the model on the processed data and evaluates its performance.

**Usage:**
1. Ensure that `data/News_Category_Dataset.json` is available in the `data` folder.
2. Run the script to train and evaluate the text classification model:

    ```bash
    python Short_Text_NN.py
    ```

### `Fabric_Defect.py`

**Description**: This script is used for detecting defects in fabric images. (Include specific details about the functionality once reviewed.)

### `Tesseract-OCR.py`

**Description**: Utilizes Tesseract OCR to extract text from images. (Include specific details about the functionality once reviewed.)

### `WebScraping.py`

**Description**: Performs web scraping to collect data from websites. (Include specific details about the functionality once reviewed.)

## Setup and Requirements

Ensure you have the required Python packages installed. You can use pip to install them:

```bash
pip install numpy pandas matplotlib scikit-learn keras tensorflow pandas_datareader tflearn
