# TIAND-SWIR  
### A Large-Scale Indian Short-Wave Infrared Dataset for Autonomous Driving

TIAND-SWIR is a real-world **Short-Wave Infrared (SWIR)** perception dataset designed to advance robust object detection for autonomous driving in challenging, unstructured Indian traffic environments.

The dataset extends the TIHAN-IITH Autonomous Navigation framework by introducing SWIR imagery to improve perception under **low light, haze, glare, and atmospheric scattering**.

---

## 🚗 Highlights

- First large-scale SWIR autonomous driving dataset from India  
- 18 days of data collection  
- ~60 hours of driving  
- 2,421+ km across 16 cities  
- 17,473 annotated images  
- 35,860 object instances  
- Urban, semi-urban, highways  
- Low illumination & fog scenarios  
- Strong baselines with YOLO models

---

## 🌙 Why SWIR?

SWIR operates in the **0.9–1.7 µm** spectral range and provides:

- better visibility in haze  
- improved contrast at night  
- reduced sensitivity to glare  
- stronger object boundaries  

This makes it ideal for safety-critical perception tasks.

---

## 🌍 Scene Coverage

TIAND-SWIR captures:

- Dense urban traffic  
- Mixed vehicle types  
- Pedestrians  
- Rural & semi-urban roads  
- Hilly regions  
- Fog & atmospheric degradation  
- Low illumination environments

---

## 🧠 Categories

The dataset includes traffic participants and infrastructure grouped into:

- People  
- Vehicles  
- Road infrastructure  
- Environmental / surface classes  

Examples include:
person, car, motorcycle, bus, truck, autorickshaw,
bicycle, tractor, animal, pushcart,
traffic sign, zebra crossing,
marked speed bump, rumblestrips, temporary barrier



The distribution naturally follows a **long-tail**, reflecting real traffic.

---

## 📊 Dataset Statistics

| Metric | Value |
|-------|------|
| Images | 17,473 |
| Instances | 35,860 |
| Avg objects / image | 2.28 |
| Max objects / image | 15 |
| Annotation | 2D bounding boxes |

---

## 🗂 Directory Structure
---
TIAND-SWIR/
├── images/
│ ├── train
│ ├── val
│ └── test
├── labels/
│ ├── train
│ ├── val
│ └── test
└── data.yaml


---

---

## 🧾 Annotation Format

YOLO style:
<class_id> <x_center> <y_center> <width> <height>


---

## 🧪 Benchmark Results

### Overall Performance

| Model | mAP@0.5 | mAP@0.5:0.95 | Precision | Recall |
|------|--------|-------------|----------|--------|
| YOLOv26 | 0.923 | 0.726 | **0.877** | 0.832 |
| **YOLOv11** | 0.925 | **0.750** | 0.787 | **0.930** |
| RT-DETR | **0.929** | 0.603 | 0.839 | 0.918 |

---

### Observations

- SWIR provides strong detection reliability in low visibility.  
- YOLOv11 offers the best strict IoU localization.  
- Transformer models achieve high coarse accuracy but may trade precision.

---

