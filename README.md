# Kidney Stone Detection using Image Processing

A MATLAB-based system that detects kidney stones in ultrasound images using classical image processing techniques, with an interactive GUI app.

---

## Overview

This project detects the presence and location of kidney stones from ultrasound images using thresholding, morphological operations, and region-of-interest (ROI) masking. The system outputs bounding boxes around detected stones along with quantitative metrics (area, centroid, mean intensity).

---

## Pipeline

### 1. Image Acquisition & Preprocessing
- Accepts JPG, PNG, JPEG input images
- Converts RGB images to grayscale
- Applies median filtering to remove speckle noise
(<img width="841" height="580" alt="image" src="https://github.com/user-attachments/assets/fcf59559-7b35-488e-bacf-cf02f3210f11" />
)

### 2. Thresholding & Morphological Processing
- Adaptive thresholding converts grayscale to binary, isolating bright regions (pixels with intensity > 220 set to white)
- Morphological closing fills gaps in detected regions
- Small artifacts removed to reduce false positives

(<img width="870" height="606" alt="image" src="https://github.com/user-attachments/assets/b5c8cd6c-79d4-4adb-9035-543c1e0eb90d" />
)

### 3. Region of Interest (ROI) Masking
- Defines a specific region most likely to contain stones
- Masks out irrelevant background, keeping only the target area


### 4. Detection & Feature Extraction
- Connected component analysis removes remaining noise
- Bounding boxes drawn around detected stone regions
- Displays "Stone Detected" or "No Stone Detected"

(<img width="974" height="699" alt="image" src="https://github.com/user-attachments/assets/ff8e526e-132f-4dfc-b2b8-ddbed9dcb164" />
)

---

## GUI Application

A standalone MATLAB App (`KidneyStoneDetectionApp.mlapp`) was built for ease of use:

(<img width="700" height="551" alt="image" src="https://github.com/user-attachments/assets/40aed253-e34f-42f6-a9b4-70aaff62913d" />
)

---
