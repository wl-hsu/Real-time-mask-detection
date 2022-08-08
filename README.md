# Real-time-mask-detection
This application can be deployed in a computer with a camera or used to analyze whether people are wearing the mask in the video. Also, this application not only detects people wearing the mask, but detects whether people are wearing it correctly and it can find out if the people use the hand or clothes to cover their face. Result and effect can refer to [final repot][https://github.com/wl-hsu/Real-time-mask-detection/blob/main/Final%20Report.pdf]


## Getting Started
### Install package

The following command will install the packages
```
$ pip install -r requirements.txt
```

### Real-time detection
The training weight provided in this application is called best.pt.
The following command will turn the camera and start detection
```
Python detect_mask_count.py --source 0 --weights best.pt
```

### Analyze video
Put the video in to target folder.
The following command will start to analyze every frame of that video.
Also, you can adjust conf as 0.x as you wish.

```
Python detect_mask_count.py --source ./target/name_of_your_video.mp4 --weights best.pt --conf 0.4
```
The analyzed video will be stored in ./runs/detect/expX

## Source
### Framework
This application is based on [yolov5][https://github.com/ultralytics/yolov5]

### Data set
[Face Mask Detection][https://www.kaggle.com/andrewmvd/face-mask-detection]

[WIDER Face dataset][http://shuoyang1213.me/WIDERFACE/]

[MAFA][https://imsg.ac.cn/research/maskedface.html]

[RMFD][https://github.com/X-zhangyang/Real-World-Masked-Face-Dataset]

### Labelling tool
[labelImg][https://github.com/heartexlabs/labelImg]


