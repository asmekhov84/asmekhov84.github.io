In the process of working on the problem of refining models of stamped parts, it became necessary to reconstruct a polygonal surface using a point cloud obtained from a [profile sensor](/professional-projects?id=10).

To solve this problem, I chose the Poisson method from the PCL library. It takes a cloud of points with normals as input and calculates an implicit function for it. Then, using this implicit function it builds a polygonal surface. It is important to note that this surface is not a triangulation, since the vertices of the triangles do not contain points of the original cloud.

This method provides a good tradeoff between time of work and quality of the resulting surface and gives a fairly smooth surface even on noisy data. The disadvantage of this method is that it always gives a closed (watertight) surface, which was not suitable for solving the task. Therefore, I added a primitive filtration by the distance from the triangles to the nearest points of the cloud, in order to remove triangles that do not have a single point nearby.

The result of the algorithm is shown in the figures below. On the example of a point cloud obtained using the virtual depth camera, you can see the results of the method before and after triangles filtration.
