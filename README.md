# real-dataset

The rotational collection device we use is as follows.

![image-20240107154517138](README.assets/image-20240107154517138.png)

Therefore, for each camera, it only involves one degree of freedom rotational movement around the axis of rotation.

The data for the middle camera is located in the path `Dataxxx/mian`.



`motor.txt` represents the absolute angular information measured by the angle encoder on the motor at corresponding times. The prior rotation angle of the camera around the rotation axis can be calculated using timestamps.



The RGB image and depth map are stored in `/color` and `/depth`, respectively. The depth map has been aligned to the RGB image, and both have a resolution of 1280*720.



`TIMESTAMP.txt` represents the timestamp.



`calibration.txt` represents the intrinsic parameters of the camera. The four values in the text correspond to fx, fy, cx, and cy.

（As the alignment of RGB and depth images has been implemented, there is only one set of intrinsic parameters.）



The file `extristrics.txt` stores the transformation relationship between the camera coordinate system and the rotation center of the camera. The upper-left `3*3` matrix represents the rotation matrix, and the `3*1` vector in the first three rows of the fourth column represents translation, with units in meters.



