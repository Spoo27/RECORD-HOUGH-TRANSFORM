# Record-HOUGH TRANSFORM

##  Aim

To implement a basic lane detection pipeline using OpenCV by completing missing code segments at specified locations.

---

##  Software Used

* Anaconda – Python 3.7
* Jupyter Notebook / VS Code
* OpenCV (cv2)
* NumPy
* Matplotlib

---

##  Algorithm 

---
Step 1: Import Libraries

Step 2: Read the Image

Step 3: Convert to Grayscale

Step 4: Display Images

Step 5: Thresholding

Step 6: Region of Interest (ROI)

Step 7: Edge Detection (Canny)

Step 8: Gaussian Blur

Step 9: Hough Transform

Step 10: Lane Detection Logic

##  Developed By

## Name: Spoorthi V
## Register No: 212224230271
---

## Program
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread('Qno. 1.jpeg')
gray_image = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Convert image to RGB for displaying
plt.title("Input Image")
plt.axis('off')

plt.imshow(gray_image, cmap='gray')
plt.title("Grayscale Image")
plt.axis('off')

edges = cv2.Canny(gray_image, 50, 150)
plt.imshow(edges, cmap='gray')
plt.title("Canny Edge Detector")
plt.axis('off')

lines = cv2.HoughLinesP(edges, 1, np.pi / 180, 100, minLineLength=50, maxLineGap=10)
for line in lines:
    x1, y1, x2, y2 = line 
    cv2.line(image, (x1, y1), (x2, y2), (0, 255, 0), 2)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))  # Image with lines drawn
plt.title("Result of Hough Transform")
plt.axis('off')
```


## Output


<img width="567" height="446" alt="image" src="https://github.com/user-attachments/assets/5a1cbd60-5439-4bfa-b1e1-4e313fc115dc" />
<img width="575" height="450" alt="image" src="https://github.com/user-attachments/assets/2ce8761a-69c2-4234-87cd-a7be28494aa8" />
<img width="567" height="445" alt="image" src="https://github.com/user-attachments/assets/419fcd2d-d44b-468f-9f02-0b8b6049615e" />
<img width="552" height="441" alt="image" src="https://github.com/user-attachments/assets/76bfffc3-9dd6-4946-9274-804f19ec4673" />

---



## Result

Thus, the lane detection pipeline is successfully implemented by completing the missing code sections. The system detects and highlights lane lines effectively.

---

