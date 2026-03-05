# 🍛 Food Calorie Detector

![Food Calorie Detector](https://img.shields.io/badge/Streamlit-App-FF4B4B?style=for-the-badge&logo=Streamlit&logoColor=white)
![YOLO](https://img.shields.io/badge/YOLO-Ultralytics-00ffff?style=for-the-badge&logo=yolo&logoColor=black)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=for-the-badge&logo=pytorch&logoColor=white)

![image alt](https://github.com/ferdianfirera/DeepLearning-ObjectDetectionForFoodCalories/blob/4a5dcce88e758374e4dbb4bd92df937ea9fd2c84/Screenshot%202026-02-09%20174208.png)

A deep learning-based web application that detects food items from images and estimates their total calories. Built with **Streamlit** and powered by state-of-the-art object detection models including **YOLO11**, **YOLO12m**, and **RT-DETR**.

## ✨ Features

- **Multi-Model Support**: Choose between RT-DETR for faster inference, YOLO11 for balanced performance, or YOLO12m for higher accuracy.
- **Custom Confidence Thresholding**: Dynamically adjust the model's confidence threshold to fine-tune detection sensitivity.
- **Calorie Estimation**: Automatically calculates and aggregates the total estimated calories based on the detected food items.
- **Interactive UI**: A sleek, user-friendly interface built with Streamlit that allows easy image uploading and instantaneous visualization of detection results.

## 🛠️ Technologies Used

- **Frontend/UI**: [Streamlit](https://streamlit.io/)
- **Computer Vision Model Framework**: [Ultralytics](https://github.com/ultralytics/ultralytics) (YOLO11, YOLO12m, RT-DETR)
- **Deep Learning Backend**: [PyTorch](https://pytorch.org/)
- **Image Processing**: OpenCV, Pillow
- **Data Handling**: Pandas, NumPy

## 📂 Project Structure

```text
├── app.py                      # Main Streamlit application
├── requirements.txt            # Python dependencies
├── Train Yolov12.ipynb         # Notebook for training YOLOv12 model
├── Traning RTDETR.ipynb        # Notebook for training RT-DETR model
├── best_food_rtdetr.pt         # Saved model weights for RT-DETR
├── best_food_yolo11.pt         # Saved model weights for YOLO11
└── best_food_yolo12m.pt        # Saved model weights for YOLO12m
```

## 🚀 Installation & Setup

### Prerequisites
- Python 3.8+

### 1. Clone the repository
```bash
git clone <repository-url>
cd <repository-directory>
```

### 2. Create a virtual environment (Recommended)
```bash
python -m venv venv
# On Windows
venv\Scripts\activate
# On macOS/Linux
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

## 💻 Usage

To run the Streamlit app locally:

```bash
streamlit run app.py
```

1. Open the provided local URL in your web browser (usually `http://localhost:8501`).
2. Use the left sidebar to **Select a Model Variant** (`RT-DETR`, `YOLO11` or `YOLO12m`) and adjust the **Confidence Threshold**.
3. Upload an image of food (JPG, JPEG, PNG).
4. View the bounding boxes around the detected foods, along with the calorie breakdown and total estimated calories.

## 🧠 Training the Models

If you wish to re-train the models or train them on a custom dataset, you can refer to the provided Jupyter Notebooks:
- **`Train Yolov12.ipynb`**: Contains the complete pipeline for training the YOLOv12 model.
- **`Traning RTDETR.ipynb`**: Contains the complete pipeline for training the RT-DETR model.

*Make sure you have your dataset formatted in the standard YOLO format and adjust the configuration files or data paths inside the notebooks accordingly.*

---
*Developed as a Capstone Project to easily detect and estimate food calories using advanced Computer Vision techniques.*
