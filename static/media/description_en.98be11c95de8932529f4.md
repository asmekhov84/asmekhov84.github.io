Recently I have already wrote about the [algorithm for extrinsic calibration of the profile sensor](/professional-projects?id=12). In that implementation the two-stage procedure was used. At the first stage, we were collecting profiles with fixed orientation of the scanner to compute it's angles, and at the second stage, we were collecting profiles with various scanner orientations to calculate it's offset.

In the new version of the algorithm I've managed to simplify this procedure, which made it possible to perform calibration using only 10-15 profiles with various positions and orientations of the scanner. The numerical optimization process is converging by all 6 target parameters simultaneously.

The animation below shows the process of searching for a solution. It can be seen how in the process of optimization the profiles are gradually approximating surface of the sphere. At the same time, computed sphere radius is approaching the true radius of the calibration sphere, which is equal to 50 mm. The final mean squared error of points deviation from the surface of the sphere is about 0.06 mm<sup>2</sup>.

The algorithm was implemented in the C++ language using the Ceres Solver library for numerical optimization. The PCL library was used for visualization.
