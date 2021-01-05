# **Truck detection using Hough and SVM**


###### Required information of Dataset source:
1. ***https://github.com/udacity/CarND-Vehicle-Detection***
2. ***http://www.gti.ssr.upm.es/data/Vehicle_database.html***
3. ***http://www.cvlibs.net/datasets/kitti/***


First we took our image array divided into car and no car.
An example is shown below

![1](https://user-images.githubusercontent.com/67842238/103686154-66a92200-4fb4-11eb-8305-3e38490b1f53.JPG)

We conver the image into a grayscale using OpenCV library
Using cv2.cvtColor().


#### **HOG FEATURE EXTRACTION AND TRAINING DATASET CREATION**

We apply HOG method on the image array to get the corners.

hog(image_gray, orientations = 11, pixels_per_cell = (16, 16), cells_per_block = (2, 2), transform_sqrt = False, 
visualize = True, feature_vector = True)

We get feature and the resultant image like below.

![Capture](https://user-images.githubusercontent.com/67842238/103686489-e7681e00-4fb4-11eb-80fd-c0c3f0a85c4d.JPG)



#### **SVM MODEL CLASSIFIER TRAINING**

We created a train ,test split and train our model LinearSVC() on the training data and also we imporved
our model using GridSearchCV to find best parameters.

We got c =100 and gamma =1 as our best parameter.



#### **TEST THE MODEL (FIND CARS)!**

We used our testing data to test the model.We took a image below 

![w](https://user-images.githubusercontent.com/67842238/103687044-a7556b00-4fb5-11eb-8904-485334221b87.JPG)

We took ou ROI by resizing the image as below.

![d](https://user-images.githubusercontent.com/67842238/103687088-b9cfa480-4fb5-11eb-9177-52c01c77aca6.JPG)

The resultant iage using our Trained SVM

![result](https://user-images.githubusercontent.com/67842238/103687236-f56a6e80-4fb5-11eb-8456-bef21b893877.JPG)



This is the final output. I am working on a better model and also working on to capture the same using my videocam.
Cheers





