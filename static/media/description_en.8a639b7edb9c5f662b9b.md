An automated welding is one of the most common applications of industrial robots. To get the maximum of this approach the robots are often equipped with sensors that allow high-quality welds, even if position and geometry of welding parts are slightly different from one to another.

There are several types of such sensors, and a profile sensor provides the most complete information about the position and geometry of the weld. The purpose of this work was to create and implement algorithms which would be able to build welding paths from a set of the profiles for various types of joints.

All algorithms I've developed are based on piecewise approximation of the profiles by a number of polynomials of the first or second order. Each of these approximated profiles gives a single point of the welding path and the corresponding approach vector.

The MATLAB environment was used for prototyping and debugging of the algorithms. Then they were implemented in the C++ language. In the pictures below you can see the results of the algorithms for the two types of welding joints: reinforced ring and the T-joint. Also on the video you can see the demonstration of how the algorithm works when welding the reinforcing cage.
