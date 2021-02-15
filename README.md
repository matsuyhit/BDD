An introduction to HASC Ballroom Dance Dataset and analysis

# About data
Ballroom dance dataset contains approximately 2.5 hours of wearable sensor data, video, and body keypoints from the video of dance performance involving 7 dancers, 13 dance figure types. Every participant wore six inertial sensors on the elbows, hips, and knees, and performed a dance amalgamation. A high-speed video camera was used to shot videos of the performances. Every participant performed 20 times: 10 times from the front of dancers, the other 10 from the back. The order of dance figures in the performance is the same among the participants.
There are 13 types of ballroom dance figures in our performance data: Open Basic, Foot change, Fan, Hockey Stick, Newyork to Right, Newyork to Left, Spot Turn, Natural Top, Opening Out, Alemana, Hand to Hand to Right, Hand to Hand to Left, Aida. The characteristics of each figure type can be seen in [Ballroom Guide](http://www.ballroomguide.com/workshop/latin/rumba.html) or in the video data. Please note that the definition of dance figures and names are sometimes different among dance councils and people. In this work, we refer to the Ballroom Guide, but you can choose any other guidelines, figure names, and figure segments if you would like.

![13steps](https://user-images.githubusercontent.com/50951418/90306956-3bdb0600-df0d-11ea-9efd-33a18e0e60e3.png)

# Downloads
You can download the files from [our website](http://hub.hasc.jp/menu). **You can use the dataset for research purposes only.**
A sample video without music is available on YouTube: https://youtu.be/SV607W_ofGE  
Label information is only annotated to the sample video on YouTube for easy understanding. 

## Contents
- csv_verxx.zip: csv files which contains wearable sensor and keypoint data
- keypoints_verxx.zip: keypoint data obtained using OpenPose
- video_verxx.zip: video data which contains 7 dancers/ 2.5 hours of record
- video_labels_verxx.zip: label data for each record corresponds to the video data
- wearable_sensor_verxx.zip: wearable sensor data attached on the six body points(right and left arms, hips, and ankles).
- sample_verxx.zip: samples of dance performance (the size of which is much smaller)

# Wearable sensor
## Size: 293 MB, Number of csv files: 7 dancers x 20 times x 6 wearable sensors = 840
CSV file that contains the time variation data of accelerometer and gyroscope sampled in 120 Hz.
There are six CSV files for each one dance performance: Left ankle, right ankle, left hip, right hip, left arm, and right arm like shown in the photos.


# Video
## Size: 101 GB, Number of videos: 7 dancers x 20 times = 140
We shot 20 times for each dancer's performance by the high speed camera(FPS: 120).
First 10 from the front and the other 10 from the back as shown in the pictures above. The picture below shows the contents in "video/dancer1/" as an example.

### Directions of video
![datacollection](https://user-images.githubusercontent.com/50951418/90306972-54e3b700-df0d-11ea-8a73-0990114a7beb.png)

### Directory example
<img width="563" alt="スクリーンショット 2020-08-25 18 20 48" src="https://user-images.githubusercontent.com/50951418/91157552-70667300-e700-11ea-9605-f0c6712d39e0.png">


# Keypoints
## Size: 4 GB, Number of folders: 7 dancers x 20 times = 140 (Each folder includes json files as many as the corresponding video frame)

From each performance video, body parts (keypoints) location data per a frame of the video are obtained using [Open Pose](https://github.com/CMU-Perceptual-Computing-Lab/openpose).

# Citation
When you use the dataset, please cite the paper below:
```
@Inbook{Matsuyama2021,
author="Matsuyama, Hitoshi
and Hiroi, Kei
and Kaji, Katsuhiko
and Yonezawa, Takuro
and Kawaguchi, Nobuo",
editor="Ahad, Md Atiqur Rahman
and Inoue, Sozo
and Roggen, Daniel
and Fujinami, Kaori",
title="A Basic Study on Ballroom Dance Figure Classification with LSTM Using Multi-modal Sensor",
bookTitle="Activity and Behavior Computing",
year="2021",
publisher="Springer Singapore",
address="Singapore",
pages="209--226",
abstract="The paper presents a ballroom dance figure classification method with LSTM using video and wearable sensors. Ballroom dance is a popular sport among people regardless of age or sex. However, learning ballroom dance is very difficult for less experienced dancers as it has many complex types of ``dance figures'', which is a completed set of footsteps. Therefore, we aim to develop a system to assist dance exercise which gives advice proper to each dance figure characteristic by recognizing dance figures correctly. While the major approach to recognize dance performance is to utilize video, we cannot simply adopt it for ballroom dance because the images of dancers overlap each other. To solve the problem, we propose a hybrid figure recognition method combining video and wearable sensors to enhance its accuracy and robustness. We collect video and wearable sensor data of seven dancers including acceleration, angular velocity, and body parts location change by pose estimation. After that, we preprocess them and put them into an LSTM-based deep learning network. As a result, we confirmed that our approach achieved an F1-score of 0.86 for 13 figure types recognition using the multi-modal sensors with trial-based fivefold cross-validation. We also performed user-based cross-validation, and sliding window algorithms. In addition, we compared the results with our previous method using Random Forest and also evaluated the robustness with occlusions. We found the LSTM-based method worked better than Random Forest with keypoint data. On the other hand, LSTM could not perform well with a sliding window algorithm. We consider the LSTM-based method would work better with a larger dance figure data, which is our next work. In addition, we will investigate how to solve occlusion problems with pose estimation.",
isbn="978-981-15-8944-7",
doi="10.1007/978-981-15-8944-7_13",
url="https://doi.org/10.1007/978-981-15-8944-7_13"
}

```

```
@inproceedings{10.1145/3341162.3344852,
author = {Matsuyama, Hitoshi and Hiroi, Kei and Kaji, Katsuhiko and Yonezawa, Takuro and Kawaguchi, Nobuo},
title = {Ballroom Dance Step Type Recognition by Random Forest Using Video and Wearable Sensor},
year = {2019},
isbn = {9781450368698},
publisher = {Association for Computing Machinery},
address = {New York, NY, USA},
url = {https://doi.org/10.1145/3341162.3344852},
doi = {10.1145/3341162.3344852},
booktitle = {Adjunct Proceedings of the 2019 ACM International Joint Conference on Pervasive and Ubiquitous Computing and Proceedings of the 2019 ACM International Symposium on Wearable Computers},
pages = {774–780},
numpages = {7},
keywords = {datasets, signal processing, machine learning},
location = {London, United Kingdom},
series = {UbiComp/ISWC ’19 Adjunct}
}
```
