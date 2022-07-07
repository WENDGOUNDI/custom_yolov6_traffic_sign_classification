# YOLOV6 trained on custom dataset: traffic sign classification

According to the official repo, YOLOv6 is a single-stage object detection framework dedicated to industrial applications, with hardware-friendly efficient design and high performance. Here we are implementing YOLOV6 in a custom dataset, the traffic sign dataset composed of 4 labels: prohibitory, danger, mandatory and others. The training has been conducted using the yolo

# Dataset
Download the dataset through this link **https://www.kaggle.com/datasets/valentynsichkar/traffic-signs-dataset-in-yolo-format**

The traffic sign dataset has four categories:
 - prohibitory
 - danger
 - mandatory
 - other

Prohibitory category consists of following Traffic Signs: speed limit, no overtaking, no traffic both ways, no trucks.

Danger category consists of following Traffic Sings: priority at next intersection, danger, bend left, bend right, bend, uneven road, slippery road, road narrows, construction, traffic signal, pedestrian crossing, school crossing, cycles crossing, snow, animals.

Mandatory category consists of following Traffic Sings: go right, go left, go straight, go right or straight, go left or straight, keep right, keep left, roundabout.

Other category consists of following Traffic Sings: restriction ends, priority road, give way, stop, no entry.

# Training steps
 - clone the yolov6 repo at https://github.com/meituan/YOLOv6
 - Get you dataset. In the data folder under the YOLOV6 folder, there will be images and labels folder. in each folder (images and labels) create train, val and test folders and move training images and labels there respectively.
 - In the data folder, modify the dataset.yaml file according to your training: number of class, class names and training paths.
 - Install the necessary libraries by running
 
 **!pip install -r requirements.txt** .
 - Check the availability of the GPU (optional).
 - Download a yolov6 model, create a folder and place it there.
 - Ensure all paths and config are set correctly and launch the training by running
 
 **!python tools/train.py --batch 16 --conf configs/yolov6s_finetune.py --data-path dataset.yaml --device 0 --epochs 10 --eval-interval 2** .
 -  Evaluate and test your trained model.
 - If the performance is weak, retrain with more data and for longer epochs.

# Inference
 For your inference, you can use the best or last weights.
![00894](https://user-images.githubusercontent.com/48753146/177731718-b320dafb-e1a5-4f4f-bb09-c3341680a4ff.jpg)
![00888](https://user-images.githubusercontent.com/48753146/177731737-8c18afb6-fe86-424f-917d-178f831ccab1.jpg)
