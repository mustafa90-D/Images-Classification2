# Images-Classification2
Multi Classes Classification

# Project Title

Nowadays, among multiple types of neural networks, CNN became state of the art in computer vision approach. It is considered as the most common approach for image classification. In this report, the CNN model will be covered, including a description of the various layers used then CNN implemented on a CIFAR images data set and results evaluated[1].

## Motivation
Nowadays, among multiple types of neural networks, CNN became state of the art in computer vision approach. It is considered as the most common approach for image classification. In this report, the CNN model  AS a human being a picture can easily be recognized to us while it is not the same for computers. Therefore, image classification in deep learning was presented to solve this challenge for computers.
Image classification defined as the way image can be analysed and recognized for a specific class by computer. It can also be defined as the possibility of image to be a part of a certain class. Normally a class is a label for example, Building, Truck, sheep and bird…….etc.
   The way computer recognizes an image is when an image is inserted like a bird image will be analysed by computer and will be able to recognize it is as a bird [2].In this project, the CNN based model will be implemented on CIFAR-10 data set for images detection
## Environment Variables

To run this project, you will need to run the following link to get acess to the main code

`https://github.com/mustafa90-D/Images-Classification2/blob/main/Last_Version-CNNMultiImage_DetectionVGG163blocksDropoout%20(1).ipynb`




## Technical Aspects
1-CNN used for images recognition for 10 diff
2-Input Features array looks like the following:

5000:images,
32:pixels hight,
32:pixelsdepth,
Colour Images type in depth RGB(Reed,Green,Blue).

3-Lable array shape looks like:
 
For each 50000 images there is one number related to the label.
10 output in the neural networks  are required to get the probability of 10 multiple classes. That is why one hot encoding was implemented  .To a set of 10 numbers from 0 to 9 the label is converted. If the image belongs to the automobile class the second number of set  will be 1:
4-The images were converted to a numbers type (float32). After that the iamges data were normalized so, the  image (x) converted to be a value between 0 and 1.As the pixels value are between 0 to 255 the pixels were divided by 255.

5-CNN Architecture:
The following architecture will be used first for our CNN model as a based model[4].


The first convolutional layer contains :
- Filter of size 3x3(Kernal size).
-Stride is one by default.
-Number of kernels is 32.
-activation function (Relu)
-padding same
 
The second layer looks like the first layer but input size will not be specified:
 
The third layer is max pooling layer:
  
-Pooling box size 2x2 which is the default value for stride.
Finally, with probability 0.25 of dropout drop out layer is added to prevent over fitting.
 
The next four layers are similar to our first four layer instead of:
Number of kernels is 64.
 Flatten layer is added to flatten pooled feature maps to one column.
 
Fully connected layer (FC) added
 - 512 neurons 
-Activation function(Relu)
 
Another dropout layer added with 0.5 probability.
 
Finally, Fully connected layer (FC) added.
-10 neurons.
-SoftMax activation.

4-Parametrs used:
-The Loss function used is ‘Categorical_Crossentropy’.

-‘Accuracy’ metrics were used to assess performance.
Optimizer used  is ‘adam’.

-Number of Itration is 500.

-Training Accuracy obtained 0.9874.

-Testing Accuracy 0.996.

