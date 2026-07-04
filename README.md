

# 🚧 Construction Safety Detection System (YOLOv8)

A custom **AI-powered computer vision system** that detects **safety helmets (hats)** and **safety jackets** in real-time using **YOLOv8**.

This project demonstrates how deep learning can be applied to **workplace safety monitoring** by automatically identifying whether construction workers are wearing required protective equipment.

---

# 📸 Demo

🎥 Video Demo:

![Demo](./demo.gif)

---

# ✨ Features

- 🦺 Detects safety helmets (hats)
- 👷 Detects safety jackets
- 🎥 Works on images and videos
- ⚡ Real-time object detection support
- 📊 Confidence score visualization
- 📦 Custom-trained YOLOv8 model
- 🔥 GPU-accelerated training (PyTorch + CUDA)
- 🧠 Transfer learning with YOLOv8m
- 📍 Bounding box visualization

---

# 🧠 Project Pipeline

```
Dataset Collection
      │
      ▼
Annotation (LabelImg / Roboflow)
      │
      ▼
YOLO Dataset Formatting (YAML config)
      │
      ▼
Model Training (YOLOv8m)
      │
      ▼
Evaluation & Validation
      │
      ▼
Inference on Images/Videos
      │
      ▼
Visualization (Bounding Boxes)
```

---

# 🛠 Tech Stack

## 💻 Programming Language
- Python

## 👁️ Computer Vision
- YOLOv8 (Ultralytics)
- OpenCV

## 🔥 Deep Learning
- PyTorch
- CUDA GPU Acceleration

## 📊 Dataset
- Custom annotated dataset

## 📓 Environment
- Google Colab

---

# 📂 Project Structure

```
Construction-Safety-Detection/
│
├── datasets/
│   ├── images/
│   ├── labels/
│   └── data.yaml
│
├── runs/
│   └── detect/
│
├── models/
│   └── best.pt
│
├── inference/
│   ├── image_test.py
│   └── video_test.py
│
├── screenshots/
│
├── README.md
└── requirements.txt
```

---

# 🚀 Training Process (Google Colab)

### 1. Install dependencies

```python
!pip install ultralytics
```

---

### 2. Import YOLO

```python
from ultralytics import YOLO
```

---

### 3. Load model

```python
model = YOLO("yolov8m.pt")
```

---

### 4. Train model

```python
model.train(
    data="data.yaml",
    epochs=100,
    imgsz=640,
    device=0
)
```

---

# 📊 Dataset Configuration (data.yaml)

```yaml
train: /content/dataset/train/images
val: /content/dataset/val/images

nc: 2
names: ["hat", "jacket"]
```

---

# 🎯 Classes Detected

- 🪖 Hat (Safety Helmet)
- 🦺 Jacket (Safety Vest)

---

# 📈 What I Learned

This project helped me gain hands-on experience in:

- Custom object detection
- YOLOv8 architecture
- Dataset annotation and preparation
- Transfer learning
- Model training and evaluation
- Real-time inference
- Computer vision pipelines
- GPU-accelerated training
- Industrial AI applications

---

# 🚀 Future Improvements

- 🔴 Real-time CCTV integration
- 📡 Edge device deployment (Jetson Nano / Raspberry Pi)
- 🚨 Alert system for missing safety gear
- 📊 Safety compliance dashboard
- ☁️ Cloud deployment
- 📱 Mobile app integration
- 🎥 Live streaming detection system
- 📦 Expand dataset (gloves, boots, goggles)
- 🧠 Improve model accuracy with YOLOv8l/x

---

# 🏗️ Real-World Use Cases

- Construction site safety monitoring
- Factory compliance detection
- Industrial hazard prevention
- Smart surveillance systems
- Workplace safety automation

---

# ⚠️ Disclaimer

This project is developed for **educational and research purposes only**.  
It should not be used as a certified safety compliance system in real industrial environments without proper validation.

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Improve model / dataset / UI
4. Submit a pull request

---

# ⭐ Support

If you like this project, consider giving it a ⭐ on GitHub!

---

# 👨‍💻 Author

**Sanaya Samadhi**

- GitHub: https://github.com/it21302862
- LinkedIn: https://www.linkedin.com/in/sanaya-samadhi/

---

# 📜 License

This project is licensed under the MIT License.