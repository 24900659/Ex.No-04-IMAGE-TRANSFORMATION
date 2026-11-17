# Ex.No-04-IMAGE-TRANSFORMATION
IMAGE TRANSFORMATION

NAME : MOHANA K.V.S.L
REG NO : 212224240093
Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

Software Required:
Anaconda - Python 3.7

Algorithm:
Step1:
Import necessary libraries such as OpenCV, NumPy, and Matplotlib for image processing and visualization.

Step2:
Read the input image using cv2.imread() and store it in a variable for further processing.

Step3:
Apply various transformations like translation, scaling, shearing, reflection, rotation, and cropping by defining corresponding functions:

1.Translation moves the image along the x or y-axis.

2.Scaling resizes the image by scaling factors.

3.Shearing distorts the image along one axis.

4.Reflection flips the image horizontally or vertically.

5.Rotation rotates the image by a given angle.

Step4:
Display the transformed images using Matplotlib for visualization. Convert the BGR image to RGB format to ensure proper color representation.

Step5:
Save or display the final transformed images for analysis and use plt.show() to display them inline in Jupyter or compatible environments.

Program:
i) Original Image
```
import cv2
import matplotlib.pyplot as plt

image = cv2.imread(r"C:\Users\mohan\Downloads\chennaii..jpg")

plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Chennai Image")
plt.axis("off")
plt.show()
```

ii)Image Translation

```
tx = 100
ty = 200

M = np.float32([[1, 0, tx],
                [0, 1, ty]])

translated_image = cv2.warpAffine(image, M, (width, height))

plt.imshow(cv2.cvtColor(translated_image, cv2.COLOR_BGR2RGB))
plt.title("Translated Image")
plt.axis("off")
plt.show()
```
iii)Image Scaling
```
fx = 2.0
fy = 2.0

scaled_image = cv2.resize(
    image, None,
    fx=fx, fy=fy,
    interpolation=cv2.INTER_LINEAR
)

plt.imshow(cv2.cvtColor(scaled_image, cv2.COLOR_BGR2RGB))
plt.title("Scaled Image")
plt.axis("off")
plt.show()
```
iv)Image shearing

```
shear_matrix = np.float32([
    [1, 0.5, 0],
    [0.5, 1, 0]
])

sheared_image = cv2.warpAffine(
    image, shear_matrix, (width, height)
)

plt.imshow(cv2.cvtColor(sheared_image, cv2.COLOR_BGR2RGB))
plt.title("Sheared Image")
plt.axis("off")
plt.show()
```
v)Image Reflection

```
reflected_image = cv2.flip(image, 1)

plt.subplot(1, 2, 1)
plt.imshow(cv2.cvtColor(image, cv2.COLOR_BGR2RGB))
plt.title("Original Image")
plt.axis("off")

plt.subplot(1, 2, 2)
plt.imshow(cv2.cvtColor(reflected_image, cv2.COLOR_BGR2RGB))
plt.title("Reflected Image")
plt.axis("off")

plt.show()
```
vi)Image Rotation
# Image Rotation
```
angle = 45

center = (width // 2, height // 2)

M = cv2.getRotationMatrix2D(center, angle, 1)

rotated_image = cv2.warpAffine(image, M, (width, height))

plt.imshow(cv2.cvtColor(rotated_image, cv2.COLOR_BGR2RGB))
plt.title("Rotated Image")
plt.axis("off")
plt.show()
```
vii)Image Cropping
```
cropped_image = image[50:250, 100:350]

plt.imshow(cv2.cvtColor(cropped_image, cv2.COLOR_BGR2RGB))
plt.title("Cropped Image")
plt.axis("off")
plt.show()
```
Output:
i) Original Image
<img width="625" height="422" alt="image" src="https://github.com/user-attachments/assets/922c3352-1cf8-4b6d-a754-079259952f62" />

ii)Image Translation
<img width="642" height="437" alt="image" src="https://github.com/user-attachments/assets/02fa9dbd-c94f-4f1e-8759-1737092105a0" />

iii) Image Scaling
<img width="652" height="446" alt="image" src="https://github.com/user-attachments/assets/8816755a-4252-493a-8789-86aac6b91cee" />

iv)Image shearing
<img width="658" height="442" alt="image" src="https://github.com/user-attachments/assets/80ea1bb1-8b6c-44c2-9191-9a3c36df8c9b" />

v)Image Reflection
<img width="658" height="247" alt="image" src="https://github.com/user-attachments/assets/12c7dd49-b7dd-4c47-b870-147960387b56" />

vi)Image Rotation
<img width="636" height="426" alt="image" src="https://github.com/user-attachments/assets/a4cc78ac-745a-4af3-b035-3b1ac66e1682" />

vii)Image Cropping
<img width="630" height="497" alt="image" src="https://github.com/user-attachments/assets/d4e13ac7-fa5e-45c9-b273-767553343b73" />

Result:
Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
