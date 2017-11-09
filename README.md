# webcam_point_features
Detection of ORB features from online webcam imges.

ORB is based on the combination of two algorithms. The FAST keypoint detector and BRIEF descriptor.

# FAST keypoint detector
This algorithm use the brightness of the pixels in order to detect a possible corner.

Initially a pixel is selected (P). The value of its brightness(Bp) is saved and a threshold value(x) is selected.

Then 16 surrounding pixels are selected. 

Only 4 of the 16 pixels are tested in order to speed up the test. The 1,5,9 and 13 will be tested.

Firstly the pixels 1 and 9 are tested. They should be more britghter(Bp+x) or darker (Bp-x). If They aren't the pixel selected(P) would not be a corner. If one of them fulfill this conditions then the other two pixels are checked. 

Three condinitions must be accomplished to consider that the pixel (P) is a corner.

This algorithm has several weaknesses. Therefore the algorithm "Machine Learning a Corner Detector" is also added for improving the perfomance.

# BRIEF (Binary Robust Independent Elementary Features)

This algorithm combined with the FAST keypoint detector is able to reduce significantly the time spent in the calculations and matching we have seen above.

