# webcam_point_features
Detection of ORB features from online webcam imges.

ORB is based on the combination of two algorithms. The FAST keypoint detector and BRIEF descriptor.

# FAST keypoint detector
This algorithm use the brightness of the pixels in order to detect a possible corner.

Initially a pixel is selected. The value of its brightness(Bp) is saved and a threshold value(x) is selected.

Then 16 surrounding pixels are selected. 

Only 4 of the 16 pixels are tested in order to speed up the test. The 1,5,9 and 13 will be tested. 

