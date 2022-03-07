# Fine-grained-localisation
In this project, we investigated the problem of fine-grained geolocation in a small indoor/outdoor environment (an art museum).

The code file mainly uses the SIFT algorithm to match the image features, find the image with the highest similarity to the test image, and obtain its coordinates to locate the test image. At the same time, the ORB is implemented for comparison.

The file is mainly run through two functions.

findBestAndExport() is used to generate the coordinates of the predicted test image obtained by comparison and save it in the csv. The required parameters are: select matchtype: orb or sift, select the hash algorithm: ahash, dhash and phash, and the ratio of matches, And the number of key points.
The findBestImage() function is used to run the matching results of a single image. After inputting the corresponding parameters and file name, you can get the matching test image and comparison image. The parameter selection is based on the FindBestAndExport with more distance threshold selection and the file name of the image

The remaining functions include:
ahash(), phash(), dhash() to calculate the hash value in three different ways
Hamming_distance() is used to calculate Hamming distance
getMathNum() is used to obtain the matches ratio
siftMatch() and orbMatch() use sift and orb respectively for feature matching
siftDraw() and orbDraw() are feature matching methods used to combine with drawing comparison diagrams
drawlines() is used to draw a comparison image