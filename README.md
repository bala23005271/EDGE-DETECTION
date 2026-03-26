# EDGE-DETECTION
## Aim:
To perform edge detection using Sobel, Laplacian, and Canny edge detectors.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1:
Import all the necessary modules for the program.

### Step2:
Load a image using imread() from cv2 module.

### Step3:
Convert the image to grayscale

### Step4:
Using Sobel operator from cv2,detect the edges of the image.

### Step5:

Using Laplacian operator from cv2,detect the edges of the image and Using Canny operator from cv2,detect the edges of the image.

### Program :
```
Name : BALA MURUGAN S
Reg No: 212223230027
import cv2
import matplotlib.pyplot as plt

# 1. Read the image using imread
# Replace 'your_image.jpg' with your actual file path
img = cv2.imread('rose.png')

# 2. Convert the color (Note: OpenCV reads in BGR, so we convert BGR to RGB for Matplotlib)
gray = cv2.cvtColor(img, cv2.COLOR_BGR2RGB)
gray_single_channel = cv2.cvtColor(img, cv2.COLOR_BGR2GRAY) # Often used for processing
gray = cv2.GaussianBlur(gray, (3,3), 0)

# --- Sobel X ---
sobelx = cv2.Sobel(gray, cv2.CV_64F, 1, 0, ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobelx)
plt.title("Sobel X axis")
plt.axis("off")
plt.show()

# --- Sobel Y ---
# 3. Complete the Sobel Y code
sobely = cv2.Sobel(gray, cv2.CV_64F, 0, 1, ksize=5) 
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(sobely)
plt.title("Sobel Y axis")
plt.axis("off")
plt.show()

# --- Sobel XY ---
sobelxy = cv2.Sobel(gray, cv2.CV_64F, 1, 1, ksize=5)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
# 4. Add the subplot command for the second image
plt.subplot(1,2,2)
plt.imshow(sobelxy)
plt.title("Sobel XY axis")
plt.axis("off")
plt.show()

# --- Laplacian ---
lap = cv2.Laplacian(gray, cv2.CV_64F)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
# 5. Display the image using imshow
plt.imshow(lap) 
plt.title("Laplacian Edge Detector")
plt.axis("off")
plt.show()

# --- Canny ---
canny = cv2.Canny(img, 120, 150) # Canny usually works best on the original or grayscale
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(gray)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(canny, cmap='gray')
# 6. Provide the title
plt.title("Canny Edge Detection") 
plt.axis("off")
plt.show()

```

## Output:
### SOBEL EDGE DETECTOR
</br>
</br>
<img width="1081" height="528" alt="Screenshot 2026-03-26 195006" src="https://github.com/user-attachments/assets/3b6064e8-f696-43d4-8636-d4d625924715" />
<img width="1043" height="544" alt="Screenshot 2026-03-26 195014" src="https://github.com/user-attachments/assets/a6c689bc-3136-4dfd-a0e1-c82470badc0c" />
<img width="1132" height="676" alt="Screenshot 2026-03-26 195452" src="https://github.com/user-attachments/assets/c8423936-be63-4665-a455-3c8f6dd37f58" />

</br>
</br>

### LAPLACIAN EDGE DETECTOR
</br>
</br>
<img width="1214" height="768" alt="Screenshot 2026-03-26 195151" src="https://github.com/user-attachments/assets/813a955a-c5ef-4d8f-9733-a954e8cc7c3c" />

</br>
</br>


### CANNY EDGE DETECTOR
</br>
</br>
<img width="1204" height="777" alt="Screenshot 2026-03-26 195907" src="https://github.com/user-attachments/assets/472f3d67-51e5-477c-9fa7-6dcb04cd1fc1" />
<img width="998" height="746" alt="Screenshot 2026-03-26 195855" src="https://github.com/user-attachments/assets/bf0426c6-4236-4dbe-882d-c513107e0ccc" />


</br>
</br>
## Result:
Thus the edges are detected using Sobel, Laplacian, and Canny edge detectors.
