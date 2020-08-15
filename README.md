An introduction to HASC Ballroom Dance Dataset and analysis

# About data
Ballroom dance dataset contains wearable sensor data, video, and body keypoints from the video of ballroom dance performance involving 7 dancers, 13 ballroom dance figure types over 100 minutes. Every participant wore six inertial sensors on the elbows, hips, and knees, and performed a dance performance. We prepared a high-speed video camera and shot videos of the performances. Every participant performed 20 times and we shot 10 times from the front of dancers, then the other 10 from the back. Also, the order of dance figures in the performance is the same among the participants.
There are 13 types of ballroom dance figures in our performance data: Open Basic, Foot change, Fan, Hockey Stick, Newyork to Right, Newyork to Left, Spot Turn, Natural Top, Opening Out, Alemana, Hand to Hand to Right, Hand to Hand to Left, Aida. The characteristics of each figure type can be seen in [Ballroom Guide](http://www.ballroomguide.com/workshop/latin/rumba.html) and also in the video data. Be careful that the definition of dance figures and names are sometimes different among dance councils. In this work, I refer to the Ballroom Guide, but you can choose any other guidelines, figure names, and figure segments if you'd like.

![13steps](https://user-images.githubusercontent.com/50951418/90306956-3bdb0600-df0d-11ea-9efd-33a18e0e60e3.png)

# Downloads
You can download the files from hub.hasc.jp. Sample data (180 MB) which contains less data (4 step types, 1 dancer) is also available.
You can use the dataset for research purposes only.

# Wearable sensor
## Size: 293 MB, Number of csv files: 7 dancers x 20 times x 6 wearable sensors = 840
CSV file that contains the time variation data of accelerometer and gyroscope sampled in 120 Hz.
There are six CSV files for each one dance performance: Left ankle, right ankle, left hip, right hip, left arm, and right arm like shown in the photos.


# Video
## Size: 101 GB, Number of videos: 7 dancers x 20 times = 140
We shot 20 times for each dancer's performance by the high speed camera(FPS: 120).
First 10 from the front and the other 10 from the back as shown in the pictures above. The picture below shows the contents in "video/dancer1/" as an example.

![datacollection](https://user-images.githubusercontent.com/50951418/90306972-54e3b700-df0d-11ea-8a73-0990114a7beb.png)

# Keypoints
## Size: 4 GB, Number of folders: 7 dancers x 20 times = 140 (Each folder includes json files as many as the corresponding video frame)

From each performance video, body parts (keypoints) location data per a frame in video are obtained using [Open Pose](https://github.com/CMU-Perceptual-Computing-Lab/openpose).

