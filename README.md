# AI for Self driving cars to interpret traffic signs
## (Traffic Sign Detection recognition and OCR)
# (please read before executing)

### Before starting with this,
Dont forget to download the preequisites to using the yolov4 model on your local machine in my YOLOV4 Tutorials 
repository link --> [Prerequisites to yolov4](https://github.com/GautamKataria/YOLOv4-Tutorials)

This repository shows how to use deep learning techniques to accomplish the task of traffic sign detection and classification by combining a custom trained Yolo-v4 model and a Convolutional Neural Network.

#### MOVE the obj.data and custom cfg file into the cfg folder in the x64 folder in your darknet build.

#### MOVE the obj.names into the data folder in the x64 folder in your darknet build.

#### MOVE the Model_30.h5 and the darknet_custom_video.py into the x64 folder.

#### MOVE the german_signs.mp4 into the data folder in the x64 folder.

Download the weights from my google drive.  LINK --> [Weights here](https://drive.google.com/file/d/1SnkVtxvIkBY-I8CxcEJHdjrOnu7qu2Jw/view?usp=sharing)

The Yolo-v4 model is custom trained on Traffic signs from the Google open images dataset. LINK--> [here](https://storage.googleapis.com/openimages/web/visualizer/index.html?set=train&type=detection&c=%2Fm%2F01mqdt)

The CNN model was trained on the German traffic-signs kaggle dataset. LINK--> [kaggle dataset](https://www.kaggle.com/meowmeowmeowmeowmeow/gtsrb-german-traffic-sign?)

## Working:-

##### Our yolov4 model is custom trained on traffic signs from the google open image dataset [Dataset for yolov4 training](https://storage.googleapis.com/openimages/web/visualizer/index.html?set=train&type=detection&c=%2Fm%2F01mqdt)
##### We use opencv to feed the video into the yolov4 model which feeds it to the custom trained yolov4 model which inturn gives us bounding boxes for traffic signs.
##### Each bounding box is then cropped from the frame and passed onto the CNN model one by one 
##### and are then classified into one of 43 different classes of traffic signs which are printed in the terminal.
##### As our yolo model also detects other signs(written signs) if the CNN model isnt quite sure that its a proper traffic sign, it passes it off to be processed and read by tesseract OCR which outputs the written text.
##### The output will be saved in the demo folder in the x64 folder in your darknet build

