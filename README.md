# Furniture Object Detection using YOLOv11
# 🪑 Furniture Object Detection using YOLOv11

An AI-powered object detection system that identifies common furniture items such as chairs, sofas, tables, beds, lamps, closets, and curtains from images using the YOLOv11 object detection model.

The project leverages **transfer learning** with a pretrained YOLOv11 model and fine-tunes it on a custom furniture dataset obtained from Roboflow.

---

## 📌 Features

- Detect multiple furniture objects in a single image
- Transfer learning using pretrained YOLOv11 weights
- Predicts:
  - Bed
  - Chair
  - Closet
  - Lamp
  - Sofa
  - Table
  - Curtain
  - Rest
- Displays bounding boxes with confidence scores
- Supports custom image testing
- Generates evaluation metrics including:
  - Precision
  - Recall
  - mAP@50
  - mAP@50-95

---

## 🧠 Model

- YOLOv11m
- Transfer Learning
- Fine-tuned on a custom furniture dataset

---

## 📂 Dataset

Dataset Source:
- Roboflow Universe

Dataset Format:
- YOLOv11

Classes:

- Bed
- Chair
- Closet
- Lamp
- Rest
- Sofa
- Table
- Curtain

Dataset Split:

- Train
- Validation
- Test

---

## 🛠 Technologies Used

- Python
- Ultralytics YOLOv11
- Roboflow
- OpenCV
- Matplotlib
- NumPy
- Google Colab

---

## 📈 Training Configuration

| Parameter | Value |
|-----------|-------|
| Model | YOLOv11m |
| Image Size | 640 × 640 |
| Epochs | 100 (Early Stopping Enabled) |
| Batch Size | 16 |
| Optimizer | AdamW |
| Transfer Learning | Yes |

---

## 📊 Evaluation Metrics

The model is evaluated using:

- Precision
- Recall
- Mean Average Precision (mAP@50)
- Mean Average Precision (mAP@50-95)

Example:

```
Precision : 86.2%
Recall    : 82.4%
mAP@50    : 89.7%
mAP50-95  : 73.5%
```

---

## 🖼 Example Prediction

Input Image

- Living room image containing multiple furniture objects.

Output

- Bounding boxes
- Object labels
- Confidence scores

Example:

```
Chair      0.95
Sofa       0.99
Table      0.97
Lamp       0.92
Curtain    0.90
```

---

## 🚀 Running the Project

### Clone Repository

```bash
git clone https://github.com/yourusername/furniture-object-detection.git
cd furniture-object-detection
```

### Install Dependencies

```bash
pip install ultralytics roboflow opencv-python matplotlib
```

### Train

```python
from ultralytics import YOLO

model = YOLO("yolo11m.pt")

model.train(
    data="data.yaml",
    epochs=100,
    imgsz=640
)
```

### Predict

```python
results = model.predict(
    source="furniture.jpg",
    conf=0.5
)
```

---

## 📁 Project Structure

```
Furniture-Object-Detection/
│
├── dataset/
│   ├── train/
│   ├── valid/
│   ├── test/
│   └── data.yaml
│
├── runs/
│   └── detect/
│       └── weights/
│           ├── best.pt
│           └── last.pt
│
├── furniture_object_detection.ipynb
├── README.md
└── requirements.txt
```

---

## 📌 Future Improvements

- Real-time webcam detection
- Video object detection
- Furniture counting
- Room inventory generation
- Mobile deployment
- ONNX/TensorRT optimization

---

## 👨‍💻 Author

**Nishitha Sathish**

Computer Science Engineering Student

---

## 📄 License

This project is intended for educational and research purposes.
