An introduction to HASC Ballroom Dance Dataset and analysis

# About data
Ballroom dance dataset contains approximately 2.5 hours of wearable sensor data, video, and body keypoints from the video of dance performance involving 7 dancers, 13 dance figure types. Every participant wore six inertial sensors on the elbows, hips, and knees, and performed a dance amalgamation. A high-speed video camera was used to shot videos of the performances. Every participant performed 20 times: 10 times from the front of dancers, the other 10 from the back. The order of dance figures in the performance is the same among the participants.
There are 13 types of ballroom dance figures in our performance data: Open Basic, Foot change, Fan, Hockey Stick, Newyork to Right, Newyork to Left, Spot Turn, Natural Top, Opening Out, Alemana, Hand to Hand to Right, Hand to Hand to Left, Aida. The characteristics of each figure type can be seen in [Ballroom Guide](http://www.ballroomguide.com/workshop/latin/rumba.html) or in the video data. Please note that the definition of dance figures and names are sometimes different among dance councils and people. In this work, we refer to the Ballroom Guide, but you can choose any other guidelines, figure names, and figure segments if you would like.

![13steps](https://user-images.githubusercontent.com/50951418/90306956-3bdb0600-df0d-11ea-9efd-33a18e0e60e3.png)

# Downloads
You can download the files from [our website](http://hub.hasc.jp/menu). **You can use the dataset for research purposes only.**

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
