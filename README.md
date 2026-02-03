# Image_Acqusition-_using_Web_Camera
## Name: HARISHBALA J
## Register no:212224223002
Aim:
 
To write a python program using OpenCV to capture the image from the web camera and do the following image manipulations.
i) Write the frame as JPG 
ii) Display the video 
iii) Display the video by resizing the window
iv) Rotate and display the video

## Software Used
Anaconda - Python 3.7
## Algorithm
### Step 1:
Import OpenCV Package.

### Step 2:
Capture Video from Webcam. Use VideoCapture(0) to access the webcam and start capturing video.

### Step 3:
Read Video or Image. Utilize 'imread' to read a video frame or image from the webcam.

### Step 4:
Save Image to File. Employ 'imwrite' to save the captured image to a file.

### Step 5:
Display Video or Image. Use 'imshow' to display the captured video frame or image.

### Step 6:
End Program with 'q'. Allow the program to be terminated by pressing the 'q' key.

## Program:

### Developed By:HARISHBALA J
### Register No:212224223002

## i) Write the frame as JPG file
```PYTHON
import cv2
import matplotlib.pyplot as plt
from IPython.display import clear_output
import time
cap = cv2.VideoCapture(0)
ret, frame = cap.read()
if ret:
    cv2.imwrite("harish.jpg", frame)
cap.release()
captured_image = cv2.imread('harish.jpg')
plt.imshow(captured_image[:,:,::-1])
plt.title('Captured Frame')
plt.axis('off')
plt.show()

```
## ii) Display the video
cap = cv2.VideoCapture(0)
```
for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    frame_rgb = cv2.cvtColor(frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```


## iii) Display the video by resizing the window
```
cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    resized_frame = cv2.resize(frame, (100, 150))  # Resize to 320x240
    frame_rgb = cv2.cvtColor(resized_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()
```

## iv) Rotate and display the video


```

cap = cv2.VideoCapture(0)

for i in range(50):
    ret, frame = cap.read()
    if not ret:
        break
    rotated_frame = cv2.rotate(frame, cv2.ROTATE_90_CLOCKWISE)
    frame_rgb = cv2.cvtColor(rotated_frame, cv2.COLOR_BGR2RGB)
    clear_output(wait=True)
    plt.imshow(frame_rgb)
    plt.axis('off')
    plt.show()
    time.sleep(0.05)

cap.release()




```
## Output

### i) Write the frame as JPG image

<img width="705" height="512" alt="Screenshot 2026-02-03 105709" src="https://github.com/user-attachments/assets/7666e8b8-5973-44f7-a517-ad0872fa77a6" />


### ii) Display the video
<img width="662" height="492" alt="Screenshot 2026-02-03 105715" src="https://github.com/user-attachments/assets/cbdd78c4-4fe5-48cd-ac41-89f10f709eec" />


### iii) Display the video by resizing the window


<img width="364" height="505" alt="Screenshot 2026-02-03 105719" src="https://github.com/user-attachments/assets/7cb1212b-e5f7-4d7b-b878-e5855510e916" />


### iv) Rotate and display the video


<img width="414" height="493" alt="Screenshot 2026-02-03 105724" src="https://github.com/user-attachments/assets/1be868eb-e030-4659-add6-ac78fe338851" />




## Result:
Thus the image is accessed from webcamera and displayed using openCV.
