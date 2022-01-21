# Lane-Detection-Using-OpenCV

## Abstract
This project uses the image and video processing module from the OpenCV library for road lane detection problems. A lane-position detection system mostly uses image processing techniques to find lane markings from the input video captured by a single camera on the vehicle's dashboard. 
The overview of the idea is to first read and decode video files into frames, i.e., converting them into a sequence of images. Then convert those sequence of images to grayscale because processing a single channel image is faster than processing a three-channel colored image. We reduce the noise using different algorithms. Then we use edge detection techniques to compute gradients in all directions of our images and trace the edges with large changes in intensity. We find the region of interest where we create a mask which is of the same dimension as our road image. Furthermore, a bitwise AND operation is performed between each pixel of our canny image and this mask. It ultimately masks the canny image and shows the region of interest traced by the polygonal contour of the mask.
At the end, we apply Hough Line transform, which is used to detect straight lines. The Probabilistic Hough Line Transform is used here, which gives output as the extremes of the detected lines.

## Aims and Objectives
The aim of this project is to avoid accidental deaths and provide a better safety on roads, by use of advanced technologies in driving assistances system. Lane detection is one of the methods which use the principle of vision-based lane detection. As the name itself indicates is a process of detecting as well as recognizing the lanes where the ground traffic circulates. For driving advanced driving assistances, the lane detection is one of the essential functions. 

## Architecture
1.	Load test images.
2.	Apply Color Selection<br />
  a.	Apply Canny edge detection.<br />
  b.	Apply Gray scaling to the images.<br />
  c.	Apply Gaussian smoothing.
3.	Perform Canny edge detection.
4.	Determine the region of interest.
5.	Apply Hough transform.
6.	Average and extrapolating the lane lines.
7.	Apply on video streams.

## Environment and Technologies
In this project we will be using Python, Jupyter Notebook and OpenCV to detect lane lines on the road in a Linux environment. I developed a processing pipeline that works on a series of individual images and applied the result to a video stream. 

## Block diagram

![image](https://user-images.githubusercontent.com/52165191/150498888-44755b43-f3ed-4223-a66c-32d5b209191c.png)

## Conclusion
In this project, A computer vision-based lane detection method was proposed. Image segmentation and remove the shadow of the road were processed. Canny operator was used to detect edges that represent road lanes or road boundaries. A series of experiment showed that the lanes were detected using Hough transformation with restricted search area and the projection of their intersection will form the last scan point called the horizon. Furthermore, in order to search out for the left and right vector points that represent the road lanes, the lane scan boundary phase uses the edge image and the left and right Hough lines and the horizon line as inputs, to effectively allocate the lane points. That was demonstrated by two hyperbola lines. The experimental results showed that the system is able to achieve a standard requirement to provide valuable information to the driver to ensure safety.
