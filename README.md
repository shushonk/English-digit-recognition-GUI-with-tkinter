# English Digit Recognition GUI with Tkinter

This software is an English digit classifier made with deep neural network using Keras and TensorFlow. The network uses MNIST dataset to recognize handwritten digits. It returns the best match and the accuracy percentage. This easy-to-use software features an interactive GUI with a built-in canvas to draw digits and displays results in an editable panel.

## Features

- **Interactive Drawing Canvas**: Draw digits using your mouse or touch input
- **Real-time Prediction**: Get instant digit recognition with accuracy scores
- **Clear Function**: Easily clear the canvas to draw new digits
- **Pre-trained Models**: Includes two trained models for comparison
- **User-friendly Interface**: Simple and intuitive GUI design

## Requirements

- Python 3.6 or higher
- TensorFlow
- Keras
- OpenCV
- PIL (Pillow)
- NumPy
- Tkinter (usually comes with Python)

## Installation

1. Install the required dependencies:
```bash
pip install tensorflow keras opencv-python pillow numpy
```

2. Download or clone this repository to your local machine.

## Usage

1. Run the application by executing:
```bash
python gui.py
```

2. The GUI window will open with a white canvas.

3. **Draw a digit** (0-9) on the canvas using your mouse.

4. **Click "Predict"** to recognize the digit and see the accuracy percentage.

5. **Click "Clear"** to erase the canvas and draw a new digit.

## Model Switching

The repository includes two pre-trained models:
- `digit_recog_cnn.h5` (CNN-based model - default)
- `deepNNmodelDigit.h5` (Deep Neural Network model)

To switch between models, edit the `tensorflowTesting.py` file and change the model name on line 8:
```python
model = tf.keras.models.load_model('digit_recog_cnn.h5')  # or 'deepNNmodelDigit.h5'
```

## How It Works

1. The application captures your drawing from the canvas.
2. The image is preprocessed (inverted, resized to 28x28 pixels, normalized).
3. The pre-trained neural network analyzes the image.
4. The model returns predictions for digits 0-9 with confidence scores.
5. The digit with the highest confidence is displayed along with its accuracy percentage.

## File Structure

```
English-digit-recognition-GUI-with-tkinter/
├── gui.py                 # Main GUI application
├── tensorflowTesting.py   # Model loading and prediction logic
├── digit_recog_cnn.h5     # CNN pre-trained model
├── deepNNmodelDigit.h5    # Deep Neural Network pre-trained model
├── image.png             # Temporary image storage for predictions
├── README.md             # This file
└── .vscode/              # VS Code settings (if applicable)
```

## Technical Details

- **Dataset**: MNIST handwritten digit dataset
- **Architecture**: Convolutional Neural Network (CNN) and Deep Neural Network
- **Input**: 28x28 grayscale images
- **Output**: 10-class classification (digits 0-9)
- **Framework**: TensorFlow with Keras API

## Troubleshooting

- If you encounter import errors, make sure all required packages are installed.
- The application saves a temporary `image.png` file during prediction, which is automatically overwritten.
- For best results, draw clear and centered digits on the canvas.

## License

This project is open source and available under the MIT License.