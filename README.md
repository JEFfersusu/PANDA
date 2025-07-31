<p align="center">
  <img src="assets/HVLO-YOLO_LOGO_01.jpg" width="600px" />
</p>

---

**Official PyTorch implementation of "HVLO-YOLO: An Ultra-Lightweight Detection Model for High-voltage Line Obstacles"**



## **Congratulations! Our HVLO-YOLO has been accepted at the BMVC'25 conference!**

## Authors

- **Weichao Pan**  
  Email: [202211107025@stu.sdjzu.edu.cn](mailto:202211107025@stu.sdjzu.edu.cn)  
  School of Computer and Artificial Intelligence, Shandong Jianzhu University, Jinan, China

- **Xu Wang**  
  Email: [202311102025@stu.sdjzu.edu.cn](mailto:202311102025@stu.sdjzu.edu.cn)  
  School of Computer and Artificial Intelligence, Shandong Jianzhu University, Jinan, China

- **Chengze Lv**  
  Email: [202311102015@stu.sdjzu.edu.cn](mailto:202311102015@stu.sdjzu.edu.cn)  
  School of Computer and Artificial Intelligence, Shandong Jianzhu University, Jinan, China

- **Zicheng Lin**  
  Email: [202311102026@stu.sdjzu.edu.cn](mailto:202311102026@stu.sdjzu.edu.cn)  
  School of Computer and Artificial Intelligence, Shandong Jianzhu University, Jinan, China

- **Gongrui Wang**  
  Email: [202311102051@stu.sdjzu.edu.cn](mailto:202311102051@stu.sdjzu.edu.cn)  
  School of Computer and Artificial Intelligence, Shandong Jianzhu University, Jinan, China

- **Xuening Zhang**  
  Email: [yukiZhang0527@outlook.com](mailto:yukiZhang0527@outlook.com)  
  School of Computer Science and Technology, Harbin Institute of Technology, Shenzhen, China

- **Yi Sun**  
  Email: [sun-y14@ulster.ac.uk](mailto:sun-y14@ulster.ac.uk)  
  School of Computing, Ulster University, Northern Ireland, United Kingdom

- **Xingbo Liu** *(Corresponding Author)*  
  Email: [sclxb@mail.sdu.edu.cn](mailto:sclxb@mail.sdu.edu.cn)  
  School of Computer and Artificial Intelligence, Shandong Jianzhu University, Jinan, China
  
> **Abstract:** With the expansion of high-voltage power grids and the increase of environmental complexity, obstacle detection on high-voltage lines has become an important task to ensure the safety of power systems. Traditional methods rely on manual feature extraction, which is difficult to deal with complex environments. Although deep learning methods improve the detection accuracy, the demand for computing resources is too high to meet the requirements of real-time and lightweight. To this end, this paper proposed an ultra-lightweight **High-Voltage Line Obstacle detection model (HVLO-YOLO)**. To achieve a better balance between detection accuracy and computational cost, three specialized lightweight modules are introduced: (1) a CSP-Partial Convolution with FourGroup module that enhances feature extraction efficiency by selectively applying partial convolution and multi-branch group strategies; (2) a Partial Convolution DownSampler module that preserves critical information during spatial resolution reduction through a dual-branch design combining max-pooling and partial convolution; and (3) a Partial Convolution Detection Head module that focuses computational resources on key feature regions through selective lightweight aggregation. These modules collaboratively reduce computational burden, minimize parameter count, and enhance obstacle detection accuracy under complex environments. Extensive experiments conducted on two benchmark datasets demonstrate that HVLO-YOLO achieves competitive detection accuracy while significantly reducing model complexity compared to state-of-the-art models.



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

---

## 🔨 Usage

### 1. Training

```bash
yolo task=detect mode=train data=cfg/datasets/HVLOD.yaml model=cfg/models/v8/HVLO-YOLO.yaml epochs=300 batch=8
```

### 2. Inference

```bash
yolo task=detect mode=predict source=datasets model=HVLO-YOLO.pt

```

## 📊 Benchmark Results

### 🛠 High-voltage Line Obstacle Dataset

| Model | Model Siez (MB) | Params (M) | FLOPs (G) | mAP50 (%) | mAP50:95 (%) |
|-------|------------|------------|-----------|-----------|--------------|
| YOLOv8-n | 6.3 | 3.0 | 8.1 | 84.6 | 63.1 |
| YOLOv10-n | 5.8 | 3.0 | 8.2 | 82.8 | 62.8 |
| **HVLO-YOLO** | **2.2** | **1.0** | **2.3** | **89.9** | **67.6** |


## 📜 Citation

If you find this work helpful, please cite:

```bibtex
@article{your_hvloyolo_2025,
  title={HVLO-YOLO: An Ultra-Lightweight Detection Model for High-voltage Line Obstacles},
  author={Pan, Weichao and Wang, Xu and Lv, Chengze and Lin, Zicheng and Wang, Gongrui and Zhang, Xuening and Sun, Yi and Liu, Xingbo},
  journal={BMVC},
  year={2025}
}
```

## 🙌 Acknowledgements

This project is inspired by the open-source efforts of YOLO, [Ultralytics](https://github.com/ultralytics/ultralytics/tree/main), and PyTorch. We thank all contributors in the community.

## 📬 Contact

For questions, feel free to reach out:

- 📧 Weichao Pan (panweichao01@outlook.com)
