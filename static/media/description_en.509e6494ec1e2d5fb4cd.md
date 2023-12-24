The purpose of this work was to create an automated quality control system for PET bottle preforms moving along a conveyor belt. In according with customer's request, data for this system must be obtained from a single RGB camera, mounted over the conveyor belt. The preforms are placed randomly on the belt. Controlled parameters are color of the preform and presence of foreign inclusions.

Since this is a fairly complex task, at the first stage it was decided to develop an algorithm for separating preform images from the background, that is, segmentation.

Preforms can be of many different shades, and also can be semitransparent. The conveyor belt has a non-uniform texture with dark and light spots. Images may have glares of various shape and size. All these factors make the task of segmentation very complicated. Under such conditions, the use of simple methods such as segmentation by brightness or by color gives an unacceptable result. Thus, it was decided to use a convolutional neural network for segmentation.

As a basis I've taken [the work](https://github.com/arahusky/Tensorflow-Segmentation/), in which authors were using a convolutional neural network to perform segmentation of images with faces. Their model, in turn, was based on the [SegNet](http://mi.eng.cam.ac.uk/projects/segnet/) architecture. The TensorFlow framework was used to implement this model.

I've adjusted the model in order to reduce number of variable parameters and, accordingly, reduce required amount of memory and training time.

To train the model, a dataset of about 100 preform images was collected and manually labeled. The image set was artificially augmented using shift, reflection and blur operations. All images were split into training and test sets in a ratio of 0.7/0.3. Segmentation results for the test set are shown in the figures below. As you can see, the trained model gives a good result even for semitransparent preforms.
