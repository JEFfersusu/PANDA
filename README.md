<p align="center">
  <img src="assets/HVLO-YOLO_LOGO_01.jpg" width="600px" />
</p>

**Official PyTorch implementation of "HVLO-YOLO: An Ultra-Lightweight Detection Model for High-voltage Line Obstacles"**

---

## 🚀 Highlights

- ✅ **Ultra-Lightweight:** Only **1.0M** parameters and **2.2MB** model size.
- ⚡ **Fast & Efficient:** Achieves **89.9% mAP50** with just **2.3 GFLOPs**.
- 📦 **Modular Design:** Three novel modules — `CP4`, `PDown`, and `PDetect`.
- 🛰️ **Field-oriented:** Designed for drone-based high-voltage obstacle detection.
- 🔁 **Generalizable:** Performs competitively on general datasets like COCO.

---

## 🔧 Installation

```bash
# Clone the repository
git clone https://github.com/JEFfersusu/HVLO-YOLO.git
cd HVLO-YOLO

# (Optional) Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install ultralytics
```

---

## 📦 High-Voltage Line Obstacle Dataset

**Download from:** [https://aistudio.baidu.com/datasetdetail/223069](https://aistudio.baidu.com/datasetdetail/223069)
