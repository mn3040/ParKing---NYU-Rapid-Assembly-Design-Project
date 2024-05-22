# Webcam Object Detection Using TensorFlow Lite

This project uses a TensorFlow Lite model to perform object detection on a live webcam feed. It draws boxes and scores around the objects of interest in each frame from the webcam. To improve FPS, the webcam object runs in a separate thread from the main program. This script works with either a Picamera or a regular USB webcam.

## Author

Matthew Nunez

## Description

This program uses a TensorFlow Lite model to perform object detection on a live webcam feed. It leverages TensorFlow Lite for model inference, OpenCV for image processing, and NumPy for numerical operations. The system runs the webcam feed in a separate thread to enhance performance.

## Libraries

- TensorFlow Lite
- OpenCV
- NumPy
- Threading

## Features

- Real-time object detection using TensorFlow Lite.
- Separate thread for webcam feed to improve frame rate.
- Bounding boxes and labels for detected objects.
- Displays center coordinates of each detected object.
- Resizable OpenCV window.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo-link
    ```

2. Navigate to the project directory:
    ```bash
    cd your-repo-link
    ```

3. Install the required packages:
    ```bash
    pip install opencv-python-headless numpy tflite-runtime
    ```

4. Ensure you have a compatible webcam connected to your system.

## Usage

1. Navigate to the project directory:
    ```bash
    cd your-repo-link
    ```

2. Run the object detection script:
    ```bash
    python TFLite_Detection_Webcam.py --modeldir=model_directory --graph=model_file.tflite --labels=labelmap.txt --threshold=0.5 --resolution=1280x720
    ```

### Command-Line Arguments

- `--modeldir`: Directory containing the `.tflite` model file.
- `--graph`: Name of the `.tflite` model file (default is `detect.tflite`).
- `--labels`: Name of the label map file (default is `labelmap.txt`).
- `--threshold`: Minimum confidence threshold for displaying detected objects (default is `0.5`).
- `--resolution`: Desired webcam resolution in `WxH` format (default is `1280x720`).
- `--edgetpu`: Use Coral Edge TPU Accelerator to speed up detection.

## Acknowledgments

- This code is based on the TensorFlow Lite image classification example at: https://github.com/tensorflow/tensorflow/blob/master/tensorflow/lite/examples/python/label_image.py
- Threading for webcam feed inspired by Adrian Rosebrock, PyImageSearch: https://www.pyimagesearch.com/2015/12/28/increasing-raspberry-pi-fps-with-python-and-opencv/

## License

This project is licensed under the MIT License. See the LICENSE file for details.

## Contact

For any inquiries or issues, please contact Matthew Nunez at [mn3040@nyu.edu](mailto:mn3040@nyu.edu).
