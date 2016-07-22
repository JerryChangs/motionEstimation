# Motion Estimation Implementation

## Description
For this project I implemented an algorithm for detecting and visualizing motion in an image sequence. Given an input of a sequence of images, it outputs a series of motion vectors which are mapped onto the images to display motion. For my implementation I divided each image into 16x16 pixel blocks, used an exhaustive block matching method to determine the block with the minimal square difference within a 7px search window. Then I mapped a motion vector corresponding to the motion detected between the two frames. The test image sequence I used was from 101 Dalmations. The main challenge in implementing this was to break down the algorithm into smaller functions that would generate the desired result without making excessive copies of the images.

## Test Cases

Test cases are written in a10_main.cpp and test each of the functions that make up motion
estimation.

1) testConstDiff() : tests the constDiff function which outputs an image of the difference between two image frames.

2) testCompareImages(): tests the compareImages function which outputs the total square difference between pixels in two images.

3) testCreateBlock(): tests the creatBlock function which outputs a 16 x 16 px block with top left corner at location x and y.

4) testSearchWindow(): tests the searchWindow function which takes a block with top left corner at location x and y and compares it to a seven pixel search window surrounding the block returning the minimum difference block.

5) testEstMotion(): tests the overall motion estimation function which takes two image and outputs the second image with motion vectors mapped on corresponding to motion within the frame. Direction of motion is marked in red.
