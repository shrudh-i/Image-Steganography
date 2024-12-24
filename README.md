# Image_Steganography

Implementing Image Steganography using Python.

# Image Steganography

This repository demonstrates the concept of **image steganography**, which involves hiding secret messages within digital images. Using this technique, a user can encode text into an image such that it is imperceptible to the human eye.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [How It Works](#how-it-works)
- [Technologies Used](#technologies-used)
- [Getting Started](#getting-started)
- [Usage](#usage)

---

## Overview
Image steganography is a method of hiding information within an image by slightly altering its pixel values. This repository implements both **encoding** (hiding the message) and **decoding** (retrieving the hidden message) functionalities. 

The key idea is to embed a message in the least significant bits (LSBs) of the image, ensuring the image quality remains visually unchanged.

---

## Features
- Hide secret messages within images using the **LSB method**.
- Retrieve hidden messages from encoded images.
- User-friendly interface with command-line interaction.
- Supports `.png` image formats for lossless encoding and decoding.

---

## How It Works
### Encoding
1. **Input Image**: The original image is selected.
2. **Secret Message**: The user inputs a text message to hide.
3. **Least Significant Bit (LSB) Manipulation**: The pixel values of the image are modified to encode the message.
4. **Output Image**: A new image is generated that contains the hidden message.

### Decoding
1. **Encoded Image**: The modified image with the hidden message is provided as input.
2. **Message Extraction**: The hidden message is extracted by reading the LSBs of the pixel values.
3. **Output**: The retrieved secret message is displayed.

---

## Technologies Used
- **Python**: Programming language for encoding and decoding logic.
- **Pillow (PIL)**: Python Imaging Library for image manipulation.
- **Numpy**: Efficient array processing for handling pixel data.

---

## Getting Started
### Prerequisites
Ensure you have Python installed on your system. You will also need the following Python libraries:
- `Pillow`
- `Numpy`

Install the dependencies by running:
```bash
pip install -r requirements.txt
```

### Usage
#### Encoding a Message
Run the encoding script:
```bash
python encode.py --image <path_to_image> --message "<your_secret_message>" --output <output_image_path>
Example:
python encode.py --image input.png --message "Hello, World!" --output encoded.png
```
The encoded.png file will be saved with the hidden message.

#### Decoding a Message
Run the decoding script:
```bash
python decode.py --image <path_to_encoded_image>
Example:
python decode.py --image encoded.png
```
The hidden message will be displayed in the terminal.
