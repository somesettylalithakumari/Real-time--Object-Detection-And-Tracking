# Real-time-Object-Detection-And-Tracking
## New Features
YOLOv5 Object Tracking Using Sort Tracker
Added Object blurring Option
Added Support of Streamlit Dashboard
Code can run on Both (CPU & GPU)
Video/WebCam/External Camera/IP Stream Supported

## Pre-Requsities
Python 3.9 (Python 3.7/3.8 can work in some cases)

This project uses the **COCO dataset** for training the YOLOv5 model, which includes:
- 80 object classes (person, car, bus, bicycle, etc.)
- Pre-trained weights for YOLOv5 are downloaded automatically or manually placed in the `yolov5/weights/` directory.

📌 **Note**: No custom dataset is needed unless training your own model.

### Future Enhancements
🔁 Upgrade to DeepSORT with re-identification

☁️ Cloud integration for remote video processing

📈 Add object analytics and heatmaps

📡 RTSP camera streaming support

🧠 Integrate anomaly detection or alerts

## Setup INstructions
1 - Clone the repository

git clone https://github.com/RizwanMunawar/yolov5-object-tracking.git
2 - Goto the cloned folder.

cd yolov5-object-tracking
3 - Create a virtual envirnoment (Recommended, If you dont want to disturb python packages)

### For Linux Users
python3 -m venv yolov5objtracking
source yolov5objtracking/bin/activate

### For Window Users
python3 -m venv yolov5objtracking
cd yolov5objtracking
cd Scripts
activate
cd ..
cd ..
4 - Upgrade pip with mentioned command below.

pip install --upgrade pip
5 - Install requirements with mentioned command below.

pip install -r requirements.txt
6 - Run the code with mentioned command below.

#for detection only
python ob_detect.py --weights yolov5s.pt --source "your video.mp4"

#for detection of specific class (person)
python ob_detect.py --weights yolov5s.pt --source "your video.mp4" --classes 0

#for object detection + object tracking
python obj_det_and_trk.py --weights yolov5s.pt --source "your video.mp4"

#for object detection + object tracking + object blurring
python obj_det_and_trk.py --weights yolov5s.pt --source "your video.mp4" --blur-obj

#for object detection + object tracking + object blurring + different color for every bounding box
python obj_det_and_trk.py --weights yolov5s.pt --source "your video.mp4" --blur-obj --color-box

#for object detection + object tracking of specific class (person)
python obj_det_and_trk.py --weights yolov5s.pt --source "your video.mp4" --classes 0
7 - Output file will be created in the working-dir/runs/detect/exp with original filename

Streamlit Dashboard
If you want to run detection on streamlit app (Dashboard), you can use mentioned command below.
Note: Make sure, to add video in the yolov5-object-tracking folder, that you want to run on streamlit dashboard. Otherwise streamlit server will through an error.

python -m streamlit run app.py
