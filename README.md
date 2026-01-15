# 📸 Image Stitching

Developed in 2025 as part of the CP461 Introduction to Computer Vision course. This project implements the Image Stitching pipeline to create a seamless Panorama view from multiple overlapping images using Homography estimation.

## 🌟 Project Overview

The core objective of this project is to understand the geometric transformations required to align different camera views into a single coordinate system. By finding common points between images, we can calculate a transformation matrix that "warps" one image to fit perfectly with another.

## 🛠 Features & Workflow

The stitching process follows these fundamental Computer Vision steps:

1. **Feature Detection & Description:** Using algorithms (SIFT) to find unique keypoints in each image.
2. **Feature Matching:** Finding corresponding points between the images using Brute-Force or FLANN matching.
3. **Homography Estimation:** Calculating the $3 \times 3$ Homography matrix ($H$) using RANSAC (Random Sample Consensus) to remove outliers and find the best alignment.
4. **Perspective Warping:** Applying the transformation matrix to warp the images into a shared canvas.
5. **Blending:** Smoothing the edges between the stitched images to create a seamless panorama.

## 🚀 Technical Implementation
* **Language:** Python
* **Core Library:** `OpenCV` (cv2)
* **Supporting Libraries:** `NumPy`, `Matplotlib`
* **Key Concepts:**
    * Planar Homography
    * Projective Transformations
    * RANSAC Algorithm
    * Image Warping

## 📚 References
* SAIJAL TOMAR (2025). [Image Stitching with OpenCV](https://www.geeksforgeeks.org/computer-vision/image-stitching-with-opencv/)
