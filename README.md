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

### vi) BGR and RGB to HSV and GRAY

```python
import cv2
img = cv2.imread('space1.jpg',1)
img = cv2.resize(img,(720,720))
cv2.imshow('Original Image',img)

hsv1 = cv2.cvtColor(img,cv2.COLOR_BGR2HSV)
cv2.imshow('BGR2HSV',hsv1)

hsv2 = cv2.cvtColor(img,cv2.COLOR_RGB2HSV)
cv2.imshow('RGB2HSV',hsv2)

gray1 = cv2.cvtColor(img,cv2.COLOR_BGR2GRAY)
cv2.imshow('BGR2GRAY',gray1)

gray2 = cv2.cvtColor(img,cv2.COLOR_RGB2GRAY)
cv2.imshow('RGB2GRAY',gray2)
cv2.waitKey(0)
cv2.destroyAllWindows()
```
### OUTPUT:

<img src="https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/64d99c6e-8d82-4245-87dc-6c5dd9392374" width=250 height=250>
<img src="https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/f49590eb-8ab2-40ec-a5cb-b8fb4fc99b9d" width=250 height=250>
<img src="https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/f7800fa9-8396-4cf5-b5df-fedf8e129141" width=250 height=250>
<img src="https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/063dfd7b-ccee-49a6-8a79-e30930440fd9" width=250 height=250>
<img src="https://github.com/Janarthanan2/DIP_EX01_COLOR_CONVERSIONS_OF-IMAGE/assets/119393515/895e84b1-9980-4291-baa1-c033331ba70f" width=250 height=250>

## Result:
Thus the images are read, displayed, and written ,and color conversion was performed between RGB, HSV and YCbCr color models successfully using the python program.







