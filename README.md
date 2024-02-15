# COLOR_CONVERSIONS_OF-IMAGE
## AIM
To write a python program using OpenCV to do the following image manipulations.

i) Read, display, and write an image.

ii) Access the rows and columns in an image.

iii) Cut and paste a small portion of the image.

iv)To perform the color conversion between RGB, BGR, HSV, and YCbCr color models.


## Software Required:
Anaconda - Python 3.7
## Algorithm:
### Step1:
Choose an image and save it as a filename.jpg ,
### Step2:
Use imread(filename, flags) to read the file.
### Step3:
Use imshow(window_name, image) to display the image.
### Step4:
Use imwrite(filename, image) to write the image.
### Step5:
End the program and close the output image windows.
### Step6:
Convert BGR and RGB to HSV and GRAY
### Step7:
Convert HSV to RGB and BGR
### Step8:
Convert RGB and BGR to YCrCb
### Step9:
Split and Merge RGB Image
### Step10:
Split and merge HSV Image

## Program:

**Developed By:** JANARTHANAN V K <br>
**Register Number:** 212222230051

## Output:

<table>
  <tr>
    <td width=50%>

### i) Read and display the image
```Python
import cv2
image=cv2.imread('japan.jpg')
image=cv2.resize(image,(1290,720))
cv2.imshow('Janarthanan V K',image)
cv2.waitKey(0)
cv2.destroyAllWindows()
``` 
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-15 203203](https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/88f86204-cb22-4b72-94a5-af6a0aaff513)


 
  </td>
  </tr>

   <tr>
    <td width=50%>

### ii) Write the image
```Python
    import cv2
    image=cv2.imread('japan.jpg')
    cv2.imwrite('d.jpg',image)
```
  </td>
  <td>

### OUTPUT:
![Screenshot 2024-02-15 204036](https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/9e2f28bf-b688-471a-97b5-849ffea08705)


  </td>
  </tr>
  <tr>
    <td width=50%>

### iii) Shape of the Image
```Python
    import cv2
    image=cv2.imread('japan.jpg',1)
    print(image.shape)
```
  </td>
  <td>

### OUTPUT:

![Screenshot 2024-02-15 205108](https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/d2318219-e727-4bf8-9c21-59bc74ae2478)

  </td>
  </tr>
  <tr>
    <td>
      
### iv) Access rows and columns
```Python
    import random
    import cv2
    image=cv2.imread('japan.jpg',1)
    image=cv2.resize(image,(400,400))
    for i in range (150,200):
      for j in range(image.shape[1]):
          image[i][j]=[random.randint(0,255),
                       random.randint(0,255),
                       random.randint(0,255)] 
    cv2.imshow('part image',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td width="50%">

### OUTPUT:

![Screenshot 2024-02-15 205437](https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/80aeca6f-9881-427a-9c19-3027d101cc0a)

  </td>
  </tr>
  <tr>
    <td width=50%>
      
### v) Cut and paste portion of image

 ```Python
    import cv2
    image=cv2.imread('japan.jpg',1)
    image=cv2.resize(image,(400,400))
    tag =image[130:200,110:190]
    image[110:180,120:200] = tag
    cv2.imshow('partimage1',image)
    cv2.waitKey(0)
    cv2.destroyAllWindows()
```
  </td>
  <td>
    
### OUTPUT:
![Screenshot 2024-02-15 210648](https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/40ec4acf-1799-4e8e-a95a-132775b8573f)

  </td>
  </tr>
</table>



## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







