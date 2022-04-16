
## Fundamental Matrix

This is the main requirement of the competition. **Finding fundamental matrix of two images**. 

### Requirements for finding fundamental matrix
1. Need keypoits identified and matched in both of the images
2. Need to convert that to pixel index into coordinates
3. Somehow incorporate global rotation and translation matrix along with camera instrinsics.

One way to do this is by following the steps and using linear algebra or opencv functions for fundamental matrix from keypoint coordinates

But what we need is a **machine learning pipeline** that can use two images, camera intrinsics and extrinsics for fundamental matrix

## Given Data

1. we have been given images of different places/monuments at different angles,scales and occlusion of the objects/keypoints.
2. Along with that a csv file containg id of the image and camera instrinsics and extrinsics for that image
3. We also have another csv file containing pair of image ids and their covisibility number (0-1) and the target column (fundamental matrix) (It's suggested to use pairs with covisibility>0.1)

## Plan
1. First thing to do would be to indentify keypoints in the image, we can use different algorithms for this but **sift** would be the obvious choice.
2. then again we will need to somehow incorporate camera intrisics and extrinsics with coordinates of the keypoints
3. Have a regression algorithm for finding fundamental matrix?
