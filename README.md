## Advanced Lane Finding
[![Udacity - Self-Driving Car NanoDegree](https://s3.amazonaws.com/udacity-sdc/github/shield-carnd.svg)](http://www.udacity.com/drive)

The goals / steps of this project are the following:  

* Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.
* Apply the distortion correction to the raw image.  
* Use color transforms, gradients, etc., to create a thresholded binary image.
* Apply a perspective transform to rectify binary image ("birds-eye view"). 
* Detect lane pixels and fit to find lane boundary.
* Determine curvature of the lane and vehicle position with respect to center.
* Warp the detected lane boundaries back onto the original image.
* Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.

---

### Dependencies

This project requires **Python 3.5** and the following Python libraries installed:

- [Jupyter](http://jupyter.org/)
- [NumPy](http://www.numpy.org/)
- [SciPy](https://www.scipy.org/)
- [scikit-learn](http://scikit-learn.org/)
- [TensorFlow](http://tensorflow.org)
- [Matplotlib](http://matplotlib.org/)
- [Pandas](http://pandas.pydata.org/) 
- [kersar](http://kersar.org/) 

Run this command at the terminal prompt to install [OpenCV](http://opencv.org/). 

## step 
each to do 

### 1.Camera calibration. Compute the camera calibration matrix and distortion coefficients given a set of chessboard images.

The camera calibration process includes the use of 20 images of a chessboard taken from different angles and distances. This process throws a list of the 3D coordinates of the inner corners (object points) in the chessboard along with a list of the corresponding 2D coordinates (image points).
![png](data.png)

### 2.对原始图像应用失真校正 Apply a distortion correction to raw images.
根据相机校准矩阵和失真系数对原始图像应用失真校正

![png](data.png)

### 3.使用颜色变换，渐变等，创建阈值二进制图像。 Use color transforms, gradients, etc., to create a thresholded binary image.
The gradient thresholding step is aimed to identify edges in the image. Since the lane lines are basically edges in the road, defining a proper thresholding with the corresponding parameters will help to define the lane lines.

<br>
  the objective is to identify pixels of a given color. To do so, ranges for the RGB channels are defined. 
 ![png](data.png)

### 4.应用透视变换来纠正二进制图像（“鸟瞰视图”）Apply a perspective transform to rectify binary image ("birds-eye view").
The images of the road have a perspective which makes the parallel lines to meet in a vanishing point. Therefore, the images need to be transformed so the lane lines are displayed parallel to each other. To do so, four points in the original image are defined; these points form a trapezoid. Other four points are defined; these points form a rectangle. The transformation consists on mapping the former points to the latter ones, so the image is transformed accordingly, and the lane lines look parallel
![png](data.png)

### 5.检测车道像素并适合查找车道边界Detect lane pixels and fit to find the lane boundary.


### 6.确定车道的曲率和相对于中心的车辆位置 Determine the curvature of the lane and vehicle position with respect to center.


![png](data.png)

### 7.将检测到的车道边界扭曲回原始图像 Warp the detected lane boundaries back onto the original image.


### 8.输出车道边界的视觉显示和车道曲率和车辆位置的数值估计 Output visual display of the lane boundaries and numerical estimation of lane curvature and vehicle position.


