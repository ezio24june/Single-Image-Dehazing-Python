# Single-Image-Dehazing-Python
python implementation of the paper: "Efficient Image Dehazing with Boundary Constraint and Contextual Regularization"

# Results
![2](https://user-images.githubusercontent.com/13918778/84451507-1cbbb180-ac08-11ea-816f-8ec983fd370d.JPG)
============================================================================================================
![1](https://user-images.githubusercontent.com/13918778/84451353-b0d94900-ac07-11ea-8f1b-3791e9f2f600.JPG)
============================================================================================================
![3](https://user-images.githubusercontent.com/13918778/84451641-8471fc80-ac08-11ea-8a7d-59f566b1c3bb.JPG)


## Installation and Running the tests

### method 1
  ```
  pip install image_dehazer
  ```
  
  **Usage:**
  ```
  $ import image_dehazer										# Load the library

  $ HazeImg = cv2.imread('image_path', 0)						# read input image
  $ HazeCorrectedImg = image_dehazer.remove_haze(HazeImg)		# Remove Haze

  $ cv2.imshow('input image', HazeImg);						# display the original hazy image
  $ cv2.imshow('enhanced_image', HazeCorrectedImg);			# display the result
  $ cv2.waitKey(0)											# hold the display window
  ```

### method 2

  1. Go to the src folder
  2. run the file "example.py"
  3. sample images are stored in the "Images/" folder
  4. Output images will be stored in the "outputImages/" folder


# Libraries needed:
  1.numpy==1.19.0
  
  2.opencv-python
  
  3.scipy

# Theory
This code is an implementation of the paper "Efficient Image Dehazing with Boundary Constraint and Contextual Regularization"
The algorithm can be divided into 4 parts:
  - Airlight estimation
  - Calculating boundary constraints
  - Estimate and refine Transmission
  - Perform Dehazing using the estimated Airlight and Transmission
  
# License
  - This project is licensed under the BSD 2 License - see the LICENSE.md file for details
  
# Acknowledgements
  - The author would like to thank Gaofeng MENG, Ying WANG, Jiangyong DUAN, Shiming XIANG, Chunhong PAN for their paper "Efficient Image Dehazing with Boundary Constraint and Contextual Regularization"
  
  - The author would like to thank Alexandre Boucaud. The function psf2otf was obtained from his repository. (https://github.com/aboucaud/pypher/blob/master/pypher/pypher.py)
  
  - The Author would like to thank Dr. Suresh Merugu for his matlab implementation of the codes. This repository is the python implementation of the matlab codes.
 
 Merugu, Suresh. (2014). Re: How to detect fog in an image and then enhance the image to remove fog?. Retrieved from: https://www.researchgate.net/post/How_to_detect_fog_in_an_image_and_then_enhance_the_image_to_remove_fog/53ae3f10d2fd64c3648b45a9/citation/download. 
