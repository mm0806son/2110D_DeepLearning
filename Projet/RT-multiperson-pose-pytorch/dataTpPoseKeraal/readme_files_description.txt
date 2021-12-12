Readme: Organization of Vicon and Kinect and Video files

Authors: Maxime Devanne (maxime.devanne@uha.fr)
         Sao Mai Nguyen (nguyensmai@gmail.com)

*************************************************
Each recordings are organised into folders that indicate the subject id. The name of the file indicates the label of the error and the recording id. The nomenclature of the files in this case is : group3/Modality/ExerciseName/ParticipantId/label\_RecordingId.extension 


1. Vicon System

1.1 Vicon skeleton
The Vicon files are acquired using Vicon Motion Capture System. 17 targets from ART were placed on the human body. The full list of target names and associated ids is:
0. Right Forearm
1. Left Forearm
2. Right Arm
3. Left Arm
4. Chest
5. Right Tigh
6. Left Tigh
7. Right Shoulder
8. Left Shoulder
9. Right Hand
10. Left Hand
11. Right Foot
12. Left Foot
13. Hips
14. Head
15. Right Tibia
16. Left Tibia

1.2 Vicon files
Each Vicon file corresponds to a motion sequence. Within the file, each row represents a frame and includes 119 floating values corresponding to the 3D global position and the global orientation (Quaternion) of each target:
x_pos y_pos z_pos x_quat y_quat z_quat w_quat
Each target's position and quaternion is concatenated according to the order described in 1.1


2. Kinect System

2.1 Kinect skeleton
The Kinect skeleton includes 25 joints:
0. SpineBase
1. SpineMid
2. Neck
3. Head
4. ShoulderLeft
5. ElbowLeft
6. WristLeft
7. HandLeft
8. ShoulderRight
9. ElbowRight
10. WristRight
11. HandRight
12. HipLeft
13. KneeLeft
14. AnkleLeft
15. FootLeft
16. HipRight
17. KneeRight
18. AnkleRight
19. FootRight
20. SpineShoulder
21. HandTipLeft
22. ThumbLeft
23. HandTipRight
24. ThumbRight

2.2 Kinect files
Each Kinect file corresponds to a motion sequence. Within the file, each row represents a frame and includes 175 floating values corresponding to the 3D position and the orientation (Quaternion) of each joint:
x_pos y_pos z_pos x_quat y_quat z_quat w_quat
Each joint's position and quaternion is concatenated according to the order described in 2.2


3. OpenPose 

3.1. OpenPose skeleton
The OpenPose skeleton used is the COCO model, from which we have recorded the following joints:
0. Head
1. mShoulder
2. rShoulder
3. rElbow
4. rWrist
5. lShoulder
6. lElbow
7. lWrist
8. rHip
9. rKnee
10. rAnkle
11. lHip
12. lKnee
13. lAnkle

3.2. OpenPose files
Each Kinect file corresponds to a motion sequence. within the file, is a dictionary of positions. The second level of dictionary is the video frame number. The third level of the dictionary is the joint name. For each joint is a 2D position :
x_pos, y_pos


