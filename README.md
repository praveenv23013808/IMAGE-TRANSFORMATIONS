# IMAGE-TRANSFORMATIONS


## Aim
To perform image transformation such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Software Required:
Anaconda - Python 3.7

## Algorithm:
## Step1:
Import the required packages.

## Step 2:
Load the image file in the program.

## Step3:
Use the techniques for Translation, Scaling, Shearing, Reflection, Rotation and Cropping using OpenCV and Python.

## Step4:
Display the modified image output.

## Step5:
End the program.

## Program:
Developed By: praveen v
Register Number: 212222233004
i)Image Translation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()
```

ii) Image Scaling
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
```


iii)Image shearing
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0.2,0],
               [0,1,0],
               [0,0,1]])
M_y=np.float32([[1, 0, 0],
                [0.5, 1, 0],
                [0,0,1]])
sheared_img_xaxis=cv2.warpPerspective(input_img,M_x,(cols,rows))
sheared_img_yaxis=cv2.warpPerspective(input_img,M_y,(cols,rows))
plt.axis('off')
plt.imshow(sheared_img_xaxis)
plt.show()
plt.axis
plt.show()
```


iv)Image Reflection
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB) 
plt.axis("off") 
plt.imshow(input_image)
plt.show()
rows, cols, dim = input_image.shape
M_x=np.float32([[1,0,0 ],
                [0,-1,rows],
                [0,0,1 ]])
M_y=np.float32([[-1,0,cols ],
                [0,1,0],
                [0,0,1 ]])
reflected_img_xaxis=cv2.warpPerspective(input_image,M_x,(cols,rows))
reflected_img_yaxis=cv2.warpPerspective(input_image,M_y,(cols,rows))
plt.imshow(reflected_img_xaxis)
plt.show()
plt.imshow(reflected_img_yaxis)
plt.show()
```



v)Image Rotation
```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("book cover.jpeg") 
input_image=cv2.cvtColor(input_image, cv2.COLOR_BGR2RGB)
angle=np.radians(45)
M=np.float32([[np.cos(angle),-(np.sin(angle)),0],
               [np.sin(angle),(np.cos(angle)),0],
               [0,0,1]])
rotated_img=cv2.warpPerspective(input_image, M, (int(cols),int(rows)))
```



vi)Image Cropping

```
import numpy as np
import cv2
import matplotlib.pyplot as plt
input_image=cv2.imread("download.jpeg") 
input_image=cv2.cvtColor(input_image,cv2.COLOR_BGR2RGB)
cropped_img=input_image[100:300, 100:300]
plt.imshow(cropped_img)


```
## Output:
### i)Image Translation
![image](https://github.com/praveenv23013808/IMAGE-TRANSFORMATIONS/assets/145824728/f6a47427-93bc-4e4a-9b3c-f69293023af4)

### ii) Image Scaling


![image](https://github.com/praveenv23013808/IMAGE-TRANSFORMATIONS/assets/145824728/fc795574-9d80-46aa-8585-7144af813c44)



### iii)Image shearing


![image](https://github.com/praveenv23013808/IMAGE-TRANSFORMATIONS/assets/145824728/04037379-6edd-44ae-8f21-37fd1dacb168)



### iv)Image Reflection


![image](https://github.com/praveenv23013808/IMAGE-TRANSFORMATIONS/assets/145824728/c3bd34b0-31aa-40f7-a77b-87e66f7c77a5)



### v)Image Rotation


![image](https://github.com/praveenv23013808/IMAGE-TRANSFORMATIONS/assets/145824728/0fb92637-0d19-4bbd-b474-e8bdc7c91a0d)




### vi)Image Cropping


![image](https://github.com/praveenv23013808/IMAGE-TRANSFORMATIONS/assets/145824728/6d93763b-ebea-4e87-be18-6a15289d77a5)





## Result: 

Thus the different image transformations such as Translation, Scaling, Shearing, Reflection, Rotation and Cropping are done using OpenCV and python programming.
