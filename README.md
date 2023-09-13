# IMPLEMENTATION-OF-FILTERSS
## Aim:
To implement filters for smoothing and sharpening the images in the spatial domain.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
### Step1
Import cv2, matplotlib.py libraries and read the saved images using cv2.imread().
 

### Step2
</br>
Convert the saved BGR image to RGB using cvtColor()
</br> 

### Step3
</br>
By using the following filters for image smoothing:filter2D(src, ddepth, kernel), Box filter,Weighted Average filter,GaussianBlur(src, ksize, sigmaX[, dst[, sigmaY[, borderType]]]), medianBlur(src, ksize),and for image sharpening:Laplacian Kernel,Laplacian Operator
</br> 

### Step4
</br>
Apply the filters using cv2.filter2D() for each respective filters.
</br> 

### Step5
</br>
Plot the images of the original one and the filtered one using plt.figure() and cv2.imshow().
</br> 

## Program:
### Developed By   : JEEVITHA E
### Register Number:2122222230054
</br>

### 1. Smoothing Filters

i) Using Averaging Filter
```
import cv2
import matplotlib.pyplot as plt
import numpy as np
image1=cv2.imread("lion.jpeg")
image2=cv2.cvtColor(image1,cv2.COLOR_BGR2RGB)
kernel=np.ones((11,11),np.float32)/121
image3=cv2.filter2D(image2,-1,kernel)
plt.figure(figsize=(8,8))
plt.subplot(1,2,1)
plt.imshow(image2)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(image3)
plt.title("Average Filter Image")
plt.axis("off")
plt.show()
```



ii) Using Weighted Averaging Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpeg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel2 = np.array([[1,2,1],[2,4,2],[1,2,1]])/16
weighted_filter = cv2.filter2D(original_image,-1,kernel2)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(weighted_filter)
plt.title("Weighted Averaging Filter Image")
plt.axis("off")






```
iii) Using Gaussian Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpeg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
gaussian_blur = cv2.GaussianBlur(src = original_image, ksize = (11,11), sigmaX=0, sigmaY=0)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(gaussian_blur)
plt.title("Gaussian Filter Image")
plt.axis("off")




```

iv) Using Median Filter
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpeg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
median = cv2.medianBlur(src=original_image,ksize = 11)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(median)
plt.title("Median Filter Image")
plt.axis("off")




```

### 2. Sharpening Filters
i) Using Laplacian Kernal
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpeg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
kernel3 = np.array([[0,1,0],[1,-4,1],[0,1,0]])
laplacian_kernel = cv2.filter2D(original_image,-1,kernel3)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_kernel)
plt.title("Laplacian kernelFiltered Image")
plt.axis("off")





```
ii) Using Laplacian Operator
```
import cv2
import numpy as np
import matplotlib.pyplot as plt
image = cv2.imread("lion.jpeg")
original_image = cv2.cvtColor(image,cv2.COLOR_BGR2RGB)
laplacian_operator = cv2.Laplacian(original_image,cv2.CV_64F)
plt.figure(figsize = (9,9))
plt.subplot(1,2,1)
plt.imshow(original_image)
plt.title("Original Image")
plt.axis("off")
plt.subplot(1,2,2)
plt.imshow(laplacian_operator)
plt.title(" Laplacian operator Filtered Image")
plt.axis("off")





```

## OUTPUT:
### 1. Smoothing Filters
</br>

i) Using Averaging Filter
</br>
</br>
![WhatsApp Image 2023-09-13 at 15 40 32](https://github.com/Jeevithaelumalai/IMPLEMENTATION-OF-FILTERSS/assets/118708245/fee9ef6d-934e-4cd8-ac86-8e212d49e89f)

</br>
</br>
</br>

ii) Using Weighted Averaging Filter
</br>
</br>
![WhatsApp Image 2023-09-13 at 15 40 53](https://github.com/Jeevithaelumalai/IMPLEMENTATION-OF-FILTERSS/assets/118708245/9b6db8e7-e2af-4ec4-b724-e2d748da66ae)

</br>
</br>
</br>

iii) Using Gaussian Filter
</br>
</br>
![WhatsApp Image 2023-09-13 at 15 41 12](https://github.com/Jeevithaelumalai/IMPLEMENTATION-OF-FILTERSS/assets/118708245/9b60f317-5541-4ac3-b056-be3f73429d9c)

</br>
</br>
</br>

iv) Using Median Filter
</br>
</br>
![WhatsApp Image 2023-09-13 at 15 41 39](https://github.com/Jeevithaelumalai/IMPLEMENTATION-OF-FILTERSS/assets/118708245/68e41c26-cd59-4149-b0e4-7f8b02defa5a)

</br>
</br>
</br>

### 2. Sharpening Filters
</br>

i) Using Laplacian Kernal
</br>
</br>
![WhatsApp Image 2023-09-13 at 15 41 59](https://github.com/Jeevithaelumalai/IMPLEMENTATION-OF-FILTERSS/assets/118708245/7544c3c0-aadc-47cd-99a7-6046c925fd67)

</br>
</br>
</br>

ii) Using Laplacian Operator
</br>
</br>
![WhatsApp Image 2023-09-13 at 15 42 19](https://github.com/Jeevithaelumalai/IMPLEMENTATION-OF-FILTERSS/assets/118708245/cef0f9a1-d450-41cf-948b-b3b0d6208c62)

</br>
</br>
</br>

## Result:
Thus the filters are designed for smoothing and sharpening the images in the spatial domain.
