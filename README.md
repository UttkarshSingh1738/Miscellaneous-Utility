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

This script detects defects in fabric images using image processing techniques. It performs the following tasks:

1. **Image Preprocessing**: Converts the image to grayscale, applies median blur, and performs adaptive thresholding.
2. **Morphological Operations**: Applies morphological closing and dilation to enhance defect contours.
3. **Defect Detection**: Finds and highlights defects based on contour area, drawing circles around detected defects.

**Usage:**
1. Place your fabric image in the specified path or modify `image_path` to point to your image.
2. Run the script to detect and visualize fabric defects:

    ```bash
    python Fabric_Defect.py
    ```

### `Tesseract-OCR.py`

This script uses Tesseract OCR to extract text from images and convert it to speech. It performs the following tasks:

1. **OCR Text Extraction**: Reads an image and extracts text using Tesseract OCR.
2. **Text-to-Speech Conversion**: Converts the extracted text to speech using Google Text-to-Speech (gTTS) and plays the audio.

**Usage:**
1. Ensure Tesseract OCR is installed and modify the path to the Tesseract executable if needed.
2. Place your image in the specified path or modify `image_path` to point to your image.
3. Run the script to extract text and hear it spoken:

    ```bash
    python Tesseract-OCR.py
    ```

### `WebScraping.py`

This script performs web scraping to collect data from a specified website. It performs the following tasks:

1. **Fetch Web Pages**: Retrieves HTML content from a series of web pages.
2. **Extract Titles and Content**: Parses the HTML to extract titles and specific sections of text.
3. **Save Results**: (Commented out) Writes the extracted content to a text file.

**Usage:**
1. Modify the URL pattern and number of chapters if needed.
2. Run the script to fetch and process web page content:

    ```bash
    python WebScraping.py
    ```

## Setup and Requirements

Ensure you have the required Python packages installed. You can use pip to install them.
