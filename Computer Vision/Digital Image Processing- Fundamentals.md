

## Dark Current
- Dark current is a current that flows even when **no photons** are incident on the camera
- Dependent on the temperatures of the sensor
- The dark current is a thermal effect and can therefore be reduced by cooling the sensor
- The longer the exposure the greater the contribution of dark current
- Dark current is also important design considerations in Machine vision systems 


### Dark Current subtraction
- Detector noise & dark current

### Shading correction
- a. shaded test pattern
- b. Estimated shading pattern
- c. product of a by the reciprocal of b

### Image multiplication and division for masking
- Digital dental X-ray image
- ROI  mask for isolating teeth with fillings


## Image Decimation and Interpolation 
- Decimation is the reduction in dimension or resolution of the image() subsampling
	- Decimation of 2, results in half the size of the original image.
	- Simples method is skipping of every other pixel.
- Interpolation is the increased in dimension or resolution of the image by averaging or other mathematical operations.
- Process of using known data to estimate values at unknown locations 
	- Interpolation of 2, results in double the resolution of the original image 
	- Simplest method is the duplication of pixels
	- More complicated method is to take the average of neighboring pixels and inserting. 

### Resizing of images
- Pixel replication
- 

### image interpolation
- Interpolation - The process of using known data to estimate values at unknown locations. 



## Pyramids
- Downsampling (decimation)
- Upsampling (interplation )


$$
\begin{array}{cc}
a &b \\
c &d
\end{array}
$$

$$
\begin{array}{cc}
1 &2 \\
3 &4
\end{array}
$$

$$
\begin{array}{cc}
1 &10 & 21 &23 \\
14 &13 &2 &21 \\
31& 33& 4& 4\\
3& 3& 4& 4
\end{array}
$$
