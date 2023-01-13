The LBR iiwa is a lightweight industrial robot, produced by the KUKA company, and designed for collaborative work with a person. The purpose of this work was to create an application that allows to simulate all movements of the robot at the programming stage. Such simulation is necessary to prevent possible collisions of the expensive manipulator with surrounding objects or with itself.

The developed application shows three-dimensional visualization of the robot's movements. The virtual model of the robot executes movement commands received either over the network or directly through the user interface. In the process of movement it's performing a collision checking and ensures that all robot's joints are within permitted ranges.

Within the project I've developed and implemented the following algorithms:

1. analytical methods for calculating forward and inverse kinematics of the robot while maintaining a given configuration;
2. methods to perform various types of movement (joint, point-to-point, linear) with maintaining a given speed.

The application was created in the Unity 3D environment. Kinematics calculation methods are called from a separate DLL written in the C++ language.
