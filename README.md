# BrandDetectAI
BrandDetectAI is a deep learning project aimed at identifying brands in images by combining OCR (Optical Character Recognition) and CNN (Convolutional Neural Networks). The tool first leverages Google Vision API’s OCR capabilities to detect any visible brand names in the text format. If no text is detected, the system utilizes a CNN model to identify the brand based on logos or other visual features. This dual-layer approach ensures robust and accurate brand detection, ideal for applications in retail, marketing, and automated brand verification.

## Features

- **OCR-Based Detection**: Uses Google Vision API to extract and recognize text in images. If a brand name matches the predefined list, it is returned as the identified brand.
- **CNN Logo Detection**: If OCR doesn’t find a brand name, the CNN model steps in to identify the brand based on logos or distinctive visual patterns.
- **High Accuracy**: The combination of OCR and CNN provides a higher accuracy rate by ensuring fallback mechanisms for brand identification.
- **Image-Based Brand Verification**: Ideal for verifying brand presence in storefronts, marketing campaigns, or product images.

## Requirements

- Python 3.x
- Google Vision API
- TensorFlow/Keras (for CNN model)
- OpenCV (for image processing)
- Other dependencies as required in `requirements.txt`

## Setup Instructions

1. **Install Dependencies**: Use `pip install -r requirements.txt` to install the necessary libraries.
2. **Google Vision API Setup**:
   - Register on Google Cloud Platform and enable the Vision API.
   - Download the service account key and set it up as per [Google Vision OCR documentation](https://cloud.google.com/vision/docs).
3. **Run the Model**:
   - Upload or specify the image containing a brand name or logo.
   - Run the `main.py` script, which will first check for text using OCR. If no text is detected, the CNN model will process the image to identify the brand based on logo features.

## Usage

```bash
python main.py --image_path <path_to_image>
```

Replace `<path_to_image>` with the path to the image file you want to analyze.

## Project Structure

- `data/`: Contains images and datasets for training the CNN model.
- `models/`: Trained CNN model and checkpoints.
- `utils/`: Helper scripts for image preprocessing and data handling.
- `main.py`: The main script that runs OCR first and then CNN for brand detection.
- `requirements.txt`: List of libraries needed to run the project.

## Future Enhancements

- Expand the CNN model to recognize additional brands and logos.
- Improve OCR matching accuracy with more robust text recognition and pattern matching.
- Integrate additional APIs for enhanced brand detection capabilities.

## License

This project is licensed under the MIT License.

