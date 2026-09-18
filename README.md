# WS-4 – Coin Detection Using OpenCV

**Name:** Thamizh S  
**Register No:** 212224040350  

## Description

This project demonstrates **coin detection using OpenCV and Python**. The input image is processed using grayscale conversion, thresholding, and morphological operations to separate the coin regions from the background. Two different approaches, **Blob Detection** and **Contour Detection**, are then used to identify and count the coins in the image.

## Technologies Used

- Python
- OpenCV
- NumPy
- Matplotlib
- Jupyter Notebook

## Methodology

The input image is first converted into grayscale and processed using thresholding. Morphological **opening** and **closing** operations are applied to reduce noise and improve the detected regions. The processed image is then analyzed using **Simple Blob Detection**, which identifies objects based on area, circularity, convexity, and inertia. **Contour Detection** is also performed using `cv2.findContours()`, with contours having an area greater than 500 pixels selected as coin candidates.

## Processing Flow

**Input Image → Grayscale → Thresholding → Morphological Processing → Blob Detection / Contour Detection → Coin Counting → Result**

## Detection Techniques

### Blob Detection

The Simple Blob Detector is configured using:

- Area filtering
- Circularity filtering
- Convexity filtering
- Inertia filtering

### Contour Detection

Contours are extracted using OpenCV's `findContours()` function. Small contours are removed using an area threshold of **500 pixels**, and the remaining contours are considered detected coin regions.

## Result

The program compares the number of coins detected using both methods. In the current notebook execution, **Blob Detection detected 0 coins**, while **Contour Detection detected 1 coin**.

## Conclusion

The project demonstrates how OpenCV image-processing techniques can be used for object detection and counting. By comparing Blob Detection and Contour Detection, the notebook shows how different computer-vision approaches can produce different detection results depending on image preprocessing and detection parameters.
