# SRP-Implementation-on-2D-image-from-3D-image
SRP implementation 
Implementation on 2D image by cropping high indesity from 3D cell images.
According to Pixel values and differences are extracted in five different patterns from image patch size of 5 × 5 pixels.
I implemented random_projection (RP) and the Final SRP Feature Descriptor. 

Global Function
The result of processing each patch is appended to the results list, which eventually contains the processed data for all 5x5 patches in the image.
Global function using image patch size of 5 × 5 pixels

XSqr
Extract the pixel values in concentric squares from the center of the patch outwards
Using an optional patch size (5x5 pixels)
The square values for the first 5 patches as a demonstration of what the processing reveals.

Circle
Takes a 5x5 pixel patch of the image as input and extracts values from concentric circles centered within the patch.
Calculates the center of the patch and iterates through radii from 0 to half the patch size, creating a mask for each circle using a distance formula from the center.
The Circle values for the first 5 patches as a demonstration of what the processing reveals.


Angular difference
Involves assessing pixel differences in an angular pattern.
Diagonal or other angular orientations within the patch to capture the texture's directionality and angular variance.
Print Angular Results


Radial Differences
Consider the distance of each pixel from the center of the patch (5x5).
Based on the differences in intensity values as a function of distance from this center pixel.
Calculate the radial descriptor by assessing the intensity values of pixels at increasing distances from the center.
Given the non-continuous nature of pixel locations and the square shape of the patch, this step involves grouping pixels by their rounded distance from the center and summarizing these groups' intensities, possibly by mean or sum.
