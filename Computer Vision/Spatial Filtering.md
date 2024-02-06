## Filtering
- Spatial filtering modifies an image by replacing the value of each pixel by a function of the values of the pixel and its neighbors.
- Refers to passing, modifying, or rejecting specified frequency components of an image.
- Linear and noon-linear filters
- can be pe..... 


## General filtering operation
- Lowpass filter
- Highpass filleter
- Bandpass filter 

### how to build each one from another
- lowpass  = lp(x,y)
- HighPass = hp(x,y) = o(x,y)-lp(x,y)
- bandpass....

## Image filtering
- A general tool for processing digital images
- One of the mostly used operations in image processing
	- Image Enhancment
	- Image analysis
	- Remove or reduce noise
	- Improve perceived....

Hypothesis: Edge = strong variation of intensity

## How to do this?
- What is impulse and impulse response?
- What is Point spred functions?


### Point spread function (PSF)
- The impulse response is often called the point spread function in image processing
- Describes the response of an imaging system to a point source or point object 
- The performance of and imaging system can be quantified by calculating ...


## Correlation and convolution
- Are two basic operations that can be performed  to extract information from images
- Almost identical operations