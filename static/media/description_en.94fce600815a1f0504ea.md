Gas engines of all modern trucks are equipped with electronic control units that get data from many different sensors and control operation of spark plugs, throttle, etc. These units store a huge number of different parameters, affecting the way they will react to sensor outputs. These parameters may be a simple scalar values, or a value tables, representing functions of two variables. These tables can only be obtained experimentally, by recording measurements on a real engine. Moreover, their values ​​may differ for various engine models.

An internal algorithms of the control unit require that such table functions were defined strictly in every point of a regular (structured) grid, i.e. with constant step by X and Y and with no gaps. However, in practice, in the process of measurement this X and Y parameters are floating because they are influenced by many other variable factors. Hence, we can't define values ​​of the table function in every (X<sub>i</sub>, Y<sub>j</sub>) node with fixed step. In addition, the registering values ​​are noised and have outliers. Thus, it is much easier to take the function values ​​in points near the required nodes of the regular grid and then fit a surface to this unstructured data. When we've interpolated data on the [irregular grid](https://en.wikipedia.org/wiki/Unstructured_grid/) we can find function values ​​at the required nodes of the regular grid. The purpose of this work was to create a handy utility that would allow to do the interpolation task.

The program I developed allows to compute values ​​of the table function of two variables in nodes of the regular grid based on the given dataset. The application can read data from the CSV file, which may have either an irregular data (unstructured scattered point cloud) or a regular data (table values ​​defined on a structured grid). There is an option to choose interpolation method and smoothing factor. When smoothing factor is greater than 0 the surface not passes through the initial points and we have an approximation, not interpolation. It's useful when data is noisy. Points with the maximum deviations are indicated by large markers. These points can be selected and removed from the set, and then interpolation will be performed again.

The program is written on the C# language and uses methods from the AlgLib library for data interpolation and OpenTK library for visualization.

Source files available in the [GitHub repository](https://github.com/asmekhov84/IGI/).