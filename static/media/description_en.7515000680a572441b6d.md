Profile sensor (2D laser scanner) is a device containing a laser projecting a straight line to the surface of an object which need to be measured, and a camera detecting the reflected light stripe. It uses the laser triangulation principle to compute (X, Z) coordinates of points along the laser stripe on the surface. Array of these points gives a profile of the object in local coordinate system of the sensor.

This type of sensor, among others, is intended for mounting on welding robots. It's using to correct a welding path, taking into account small deviations in geometry of a weld. Also it can be used to monitor parameters and quality of a weld. The purpose of this work was to create the utility that would allow a user to work with the profile sensor developed by the Eidos Robotics company.

The implemented application allows to configure the camera module (exposure time, gamma-correction and others), perform the intrinsic calibration of the profile sensor in manual and semi-automatic modes, and also monitor parameters of welding joints of various types.

Within the project, I developed and implemented the following algorithms:

1. localization of the laser stripe on the image, which can work even with images containing glare;
2. compensation of the camera lens distortion;
3. intrinsic profile sensor calibration, which includes calculation of the homography matrix to transform coordinates from the plane of the CMOS sensor to the laser plane;
4. localization of welding joints of four different types.

In addition, I developed the entire application user interface (the Qt framework was used), and also the convenient wrapper for the camera API (the Basler industrial camera was used), which includes methods for camera connection/disconnection, internal parameters configuration and image capturing.
