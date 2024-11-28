# Face Detection and Dataset Management Project

Welcome to the **Face Detection and Dataset Management Project**! This project is designed for face detection, anti-spoofing classification, and dataset preparation for machine learning models. With real-time processing and dataset splitting, this project streamlines your AI training pipeline.

---

## 🌟 Features

1. **Face Detection with Quality Filtering**  
   - Detects faces using `cvzone.FaceDetector`.
   - Measures blurriness to ensure only high-quality images are saved.
   - Normalizes bounding box coordinates and saves labels in YOLO format.

2. **Real-Time Anti-Spoofing Detection**  
   - Classifies faces as `fake` or `real` using a YOLO model.
   - Displays bounding boxes, classifications, and confidence percentages on live video feeds.

3. **Dataset Splitting**  
   - Splits datasets into `train`, `val`, and `test` folders.
   - Generates a `data.yaml` file for YOLO model training compatibility.
   - Supports multi-class datasets, such as `fake` and `real`.

---

## 🛠️ Setup Instructions

### Prerequisites

Before getting started, make sure you have the following installed:
- Python 3.8+
- OpenCV
- cvzone
- Ultralytics YOLO
- NumPy
- shutil

### Installation Steps

1. **Clone the Repository**  
   ```bash
   git clone <repository_url>
   cd <repository_directory>
Install Dependencies

bash
Copy code
pip install opencv-python cvzone ultralytics
Place Your YOLO Model
Ensure your YOLO model file (best.pt) is in the correct directory as specified in the scripts.

🚀 Usage Guide
1. Face Detection and Image Collection
Detect faces and save high-quality images:

bash
Copy code
python face_detection.py
Images are saved in Dataset/DataCollect/ along with YOLO labels.
2. Real-Time Anti-Spoofing Detection
Classify faces into fake or real using the YOLO model:

bash
Copy code
python anti_spoofing.py
Results are displayed live with bounding boxes and confidence percentages.
3. Dataset Splitting
Prepare your dataset for training, validation, and testing:

bash
Copy code
python dataset_split.py
Adjust the split ratio in the splitRatio variable in the script.
Output is saved in Dataset/Split_Data/.
⚙️ Configuration Options
Blurriness Threshold
Adjust the blurThreshold variable in face_detection.py to filter images based on clarity.
Example:

python
Copy code
blurThreshold = 35  # Higher value for sharper images
Confidence Threshold
Update the confidence variable in both scripts to modify classification sensitivity.
Example:

python
Copy code
confidence = 0.8  # Minimum confidence for detection
Dataset Split Ratios
Change the split ratios for training, validation, and testing in dataset_split.py.
Example:

python
Copy code
splitRatio = {"train": 0.7, "val": 0.2, "test": 0.1}
📂 Directory Structure
bash
Copy code
.
├── Dataset/
│   ├── all/                 # Raw images and labels
│   ├── DataCollect/         # Collected images and labels
│   └── Split_Data/          # Train, val, and test splits
├── Model/
│   └── best.pt              # YOLO model file
├── face_detection.py        # Script for face detection
├── anti_spoofing.py         # Script for anti-spoofing detection
├── dataset_split.py         # Script for dataset splitting
└── README.md                # This file
📄 Output Examples
Face Detection Output
Saved images: Dataset/DataCollect/<timestamp>.jpg
YOLO label files: Dataset/DataCollect/<timestamp>.txt
Dataset Split Output
Train data: Dataset/Split_Data/train/
Validation data: Dataset/Split_Data/val/
Test data: Dataset/Split_Data/test/
Example data.yaml File:
yaml
Copy code
path: ../Data
train: ../train/images
val: ../val/images
test: ../test/images

nc: 2
names: ['fake', 'real']

## 🤝 Acknowledgments

OpenCV: For efficient image processing.
cvzone: Simplifying bounding box visualization.
Ultralytics YOLO: Powering real-time classification.

### For questions or suggestions, feel free to reach out or create an issue in the repository. Happy coding! 🎉

# Training 

![](https://github.com/Vaibhav112003/Anti_Spoofing_Project-/blob/main/training_Dataset.png)

# Result 

![Repository Logo](https://github.com/Vaibhav112003/Anti_Spoofing_Project-/blob/main/result1.png)


