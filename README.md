# Image Alignment and Cropping Tool

## Overview
This Python tool automates the process of aligning and cropping images. It is particularly useful for images containing a central rectangular object surrounded by transparency. The tool centers this rectangle within each image's dimensions and then crops the image around this centered rectangle, standardizing the format and focus across a series of images.

## Features
- **Automated Alignment**: Centers a rectangular object within each image.
- **Cropping**: Crops the image around the centered rectangle.
- **Batch Processing**: Processes multiple images in a specified directory.
- **Format Support**: Compatible with `.png`, `.jpg`, and `.jpeg` image formats.

## Prerequisites
- Python 3.x
- Pillow (Python Imaging Library Fork)

## Installation

### Python Installation
Ensure Python 3.x is installed on your system. If not, download and install it from [python.org](https://www.python.org/downloads/).

### Pillow Installation
Install the Pillow library using pip. Run the following command:

```bash
pip install Pillow
```

## Usage Instructions

1. **Set Source and Destination Directories**:
   - Modify `source_dir` in the script to the directory containing the images.
   - Modify `dest_dir` in the script to your desired output directory.

2. **Execute the Script**:
   - Run the script in a Python environment. This can be through a Python IDE or via the command line.

    ```bash
    python script_name.py
    ```

3. **Check Output**:
   - Processed images will be saved in the specified destination directory.

## Script Overview

The script performs the following operations on each image:

- Identifies the bounding box of the non-transparent rectangle.
- Calculates the centers of the rectangle and the image.
- Aligns the rectangle's center with the image's center.
- Crops the image to focus on the centered rectangle.
- Saves the processed image in PNG format to preserve transparency.

## Configuration

- **Image Formats**: The script currently supports `.png`, `.jpg`, and `.jpeg` formats. You can modify the code to include additional formats if necessary.
- **Customization**: Advanced users can modify the script for different image processing needs, like changing the method of determining the central object.

## Note

- The effectiveness of the tool relies on the assumption that the most significant non-transparent part of each image is the rectangle that needs to be centered.
- Ensure that the specified directories exist and you have read/write permissions.

## License
[MIT License](LICENSE)

---

For any queries or contributions, please open an issue or a pull request on this repository.
