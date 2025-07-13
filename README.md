# Emojify

Emojify is a facial expression recognition project that uses deep learning to match human facial expressions with corresponding emojis in real time. This project leverages a Convolutional Neural Network (CNN) trained on grayscale images to classify emotions and provides a simple GUI to visualize the detected emotion with an emoji overlay.

## Features

- Detects facial expressions from webcam video feed.
- Classifies emotions into seven categories: Angry, Disgusted, Fearful, Happy, Neutral, Sad, Surprised.
- Maps detected emotions to corresponding emojis and displays them in a GUI.
- Built using TensorFlow/Keras, OpenCV, and Tkinter.
- Includes scripts for both model training and inference with GUI.

## Getting Started

### Prerequisites

- Python 3.9+
- pip (Python package manager)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/Shashankkusu/Emojify.git
   cd Emojify
   ```

2. **Install required packages**
   ```bash
   pip install numpy opencv-python tensorflow matplotlib pillow
   ```

3. **Prepare Data**
   - Place your training and test images in the `data/train` and `data/test` directories, organized by emotion labels.

### Model Training

To train the emotion recognition model:

- Open `ModelTraining.ipynb` in Jupyter Notebook.
- Run all cells to initialize the data generators, build and train the CNN model, and save the trained weights (`recognition_model.h5`).

### Running the GUI

To run the Emojify application with GUI:

1. Ensure the trained model weights (`recognition_model.h5`) are present in the working directory.
2. Open and run `Emojify_GUI.ipynb` in Jupyter Notebook.
   - The webcam feed will open in a Tkinter window.
   - The app will detect your facial expression and display the corresponding emoji.

## Emotion Categories

| Label      | Description  |
|------------|--------------|
| 0          | Angry        |
| 1          | Disgusted    |
| 2          | Fearful      |
| 3          | Happy        |
| 4          | Neutral      |
| 5          | Sad          |
| 6          | Surprised    |

## Project Structure

```
.
├── data/
│   ├── train/
│   └── test/
├── ModelTraining.ipynb
├── Emojify_GUI.ipynb
├── recognition_model.h5
├── LICENSE
```

- `ModelTraining.ipynb`: Jupyter notebook for model training.
- `Emojify_GUI.ipynb`: Jupyter notebook for running the GUI with emotion-to-emoji mapping.
- `recognition_model.h5`: Saved weights for the trained model.
- `data/`: Training and testing images organized by emotion label.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- Built with TensorFlow/Keras and OpenCV.
- Emoji images are required for mapping emotions in the GUI (ensure you have appropriate emoji image files).
