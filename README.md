# WORKSHOP 3 – Canny Edge Detection

## Aim

To implement the Canny Edge Detection algorithm using Python and OpenCV on a sample image to detect and analyze the edges present in the image.

## Software Required

- Python
- OpenCV
- Matplotlib
- Jupyter Notebook

## Procedure

1. Import the required Python libraries.
2. Read the input image using OpenCV.
3. Display the original image.
4. Convert the original image into grayscale.
5. Apply the Canny Edge Detection algorithm using suitable threshold values.
6. Display the detected edge image.
7. Compare the original image with the Canny edge-detected image.
8. Analyze how the threshold values affect the detected edges.

## Program


## Develop by : ARSHATH HUSSAIN I
## Reg no: 212224230022


### Display Original Image

```
import cv2
import numpy as np
import matplotlib.pyplot as plt

image = cv2.imread('images.jpg') 
image_rgb = cv2.cvtColor(image, cv2.COLOR_BGR2RGB)

plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")
plt.show()


```
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/cfbd7630-a012-4573-8a5f-5c8281a9cc75" />


```


`gray = cv2.cvtColor(image, cv2.COLOR_BGR2GRAY)

edges = cv2.Canny(gray, 100, 200)

plt.imshow(edges, cmap="gray")
plt.title("Canny Edge Detection")
plt.axis("off")
plt.show()

```
<img width="389" height="411" alt="download" src="https://github.com/user-attachments/assets/8582548e-7d19-4416-b814-842cc4e41e58" />


```



plt.figure(figsize=(12, 5))

plt.subplot(1, 2, 1)
plt.imshow(image_rgb)
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(edges, cmap="gray")
plt.title("Canny Edge Detection")
plt.axis("off")

plt.show()

```
<img width="912" height="427" alt="download" src="https://github.com/user-attachments/assets/b82b8e9b-8d1e-4ada-9026-edd04698065b" />


## Result
The Canny Edge Detection algorithm was successfully implemented using Python and OpenCV. The edges and boundaries of objects in the input image were detected successfully. The original image and the edge-detected image were compared to clearly observe the detected edges.

The threshold values 100 and 200 were used in the Canny function. Lower threshold values detect more edges and fine details, while higher threshold values detect fewer and stronger edges.



