
# 🛵 Two-Wheeler Number Plate Detection using YOLOv11 (v1)

## 📌 Project Summary

This project is focused on detecting **two-wheeler number plates** using a custom-trained **YOLOv11** object detection model.  
It uses a specialized dataset containing images of bikes, scooters, and other two-wheeled vehicles with visible license plates.

- 🔍 Real-time detection on videos and images.
- ⚙️ Trained using a custom dataset from [Roboflow](https://universe.roboflow.com/hari-i4xuq/license_plate-2-wheeler).
- 🧠 Based on YOLOv11 for fast and efficient object detection.

> 🔧 **Note:** This is **version 1 (v1)**. While the model works in many cases, detection accuracy is not yet perfect. We’re actively working to improve performance across lighting, angles, and varied plate types.

---

## 🛠️ Setup Instructions

### 📁 1. Download the Dataset

- Link: [Yolov11 Model Download](https://github.com/ultralytics/assets/releases/download/v8.3.0/yolo11m.pt)
- Link: [Roboflow Dataset - License Plate 2-Wheeler](https://universe.roboflow.com/hari-i4xuq/license_plate-2-wheeler)
- Format: Select **YOLOv11 PyTorch** format.
- Extract the ZIP file and upload it to **Google Colab** in the next step.

---

### ⚙️ 2. Train the Model using Google Colab

> Colab Notebook: `dataset_and_train.ipynb` (included in this repo)

1. Upload the Roboflow dataset (train/valid/test folders and `data.yaml`) to Colab.
2. Open the notebook and follow step-by-step code to train the model.
3. After training, download the weights from:

```
/runs/detect/train/weights/best.pt
```

---

### 🧪 3. Run Inference on Local Jupyter Notebook

> Test Notebook: `test.ipynb` (included in this repo)

#### Folder Structure:

```
two-wheeler-number-plate-detection/
├── best.pt                # Trained YOLOv11 weights
├── test.ipynb             # Inference script
├── dataset_and_train.ipynb
├── test_images/           # Folder with test images
│   ├── test1.jpg
│   └── test2.jpg
├── sample_video.mp4       # Optional: For video detection
```

#### How to Run:

1. Open `test.ipynb` in Jupyter Notebook or Colab.
2. Make sure `best.pt` is in the same directory.
3. The notebook will:
   - Load YOLOv11 model
   - Run detection on images from `test_images/`
   - Show image with bounding boxes around number plates

---

## 🧩 Dependencies

Install required libraries in your environment:

```bash
pip install ultralytics opencv-python matplotlib torch easyocr 
```

---

## 🔄 Output Example

### ✅ Detected Image:
<img src="https://github.com/manavsoni05/Two-Wheeler-Number-Plate-Detection/blob/main/Test-Image.png" width="500"/>

### 🎞️ Detected Video Frame:
<img src="https://github.com/manavsoni05/Two-Wheeler-Number-Plate-Detection/blob/main/Test-Image-02.png" width="500"/>

---

## 🧠 Future Improvements (Coming Soon)

- Improve detection accuracy across various plate formats.
- Handle low-light, blurry, and angled cases better.
- Export detections to CSV or Excel with timestamp & plate number.
- Add Realtime Detection & End to end Dashboard for Live Feed and License Plate Detection.

---

## 👨‍💻 Author

**Manav Soni**  
B.Tech - AIML | Charotar University of Science and Technology  
Reach out: [LinkedIn](https://www.linkedin.com/in/manavsoni05) 

---

## 📄 License

This project is for educational and research use only. Commercial usage requires proper dataset license and legal plate data compliance.
