# AI Image Classifier

An AI-powered application that classifies images using a pre-trained MobileNetV2 model.

## Features

- Upload and analyze images in JPG or PNG format
- Utilizes MobileNetV2 architecture pre-trained on ImageNet
- Provides top-3 predictions with confidence scores
- User-friendly interface built with Streamlit

## Demo

![AI Image Classifier Screenshot](https://via.placeholder.com/800x400?text=AI+Image+Classifier+Screenshot)

## Requirements

- Python 3.8 or higher
- TensorFlow 2.x
- OpenCV (cv2)
- Streamlit
- NumPy
- Pillow (PIL)

## Installation

1. Clone the repository:
```bash
git clone https://github.com/YourUsername/AI_Image_Classifier.git
cd AI_Image_Classifier
```

2. Create a virtual environment and activate it:
```bash
# Create virtual environment
python -m venv venv

# Activate on Windows
venv\Scripts\activate

# Activate on macOS/Linux
source venv/bin/activate
```

3. Install dependencies:
```bash
# Using pip
pip install -r requirements.txt

# Or manually install required packages
pip install tensorflow opencv-python streamlit numpy pillow
```

## Usage

1. Run the Streamlit application:
```bash
streamlit run main.py
```

2. Open the application in your web browser (typically http://localhost:8501)

3. Upload an image using the file uploader

4. Click "Classify Image" to analyze the image

5. View the top-3 predictions with confidence percentages

## How It Works

1. **Image Upload**: User uploads an image through Streamlit's interface
2. **Preprocessing**: 
   - The image is converted to a NumPy array
   - Resized to 224x224 pixels (MobileNetV2's required input size)
   - Preprocessed using TensorFlow's built-in preprocessing function
   - Expanded to include batch dimension
3. **Model Prediction**: 
   - The preprocessed image is fed into the MobileNetV2 model
   - The model produces prediction scores for 1000 ImageNet classes
4. **Results Display**:
   - Top 3 predictions are decoded into human-readable labels
   - Results are displayed with confidence percentages

## Project Structure

```
image_classifier/
├── main.py          # Main application code
├── README.md        # Project documentation
├── requirements.txt # Dependencies
└── samples/         # Sample images for testing (optional)
```

## Troubleshooting

- **Memory Issues**: If you encounter memory problems, try reducing the batch size or using a lighter model
- **Compatibility**: Make sure your TensorFlow version is compatible with your CUDA/cuDNN if using GPU acceleration
- **Image Format**: If your image isn't recognized, ensure it's a valid JPG or PNG file

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- MobileNetV2 model from TensorFlow/Keras Applications
- ImageNet dataset for pre-trained weights
- Streamlit for the web application framework