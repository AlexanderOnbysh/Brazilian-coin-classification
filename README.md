# Brazilian-coin-classification
The idea is to explore a classification problem for a single coin and a regression problem for a group of coins, trying to count how much money they sum.
Idea was taken from [Brazilian Coins](https://www.kaggle.com/lgmoneda/br-coins)

## Pipeline
1. Background masking
2. Coin segmentation
3. Image augmentation
4. Train model
5. Test on classification and regression datasets
---
Original image:


![original image](https://github.com/OnbyshAlex/Brazilian-coin-classification/blob/master/images/original.jpg)
### Background masking
Use HSV format to select proper threshold for background masking.


![masked background](https://github.com/OnbyshAlex/Brazilian-coin-classification/blob/master/images/masking.jpg)

### Coin segmentation
Use Hough transform to find circle objects on image.


![circles](https://github.com/OnbyshAlex/Brazilian-coin-classification/blob/master/images/circles.jpg)

## Predictive models
SVM on radiuses of coins shows **≈60%** accuracy

## Image augmentation
<img src="https://github.com/OnbyshAlex/Brazilian-coin-classification/blob/master/images/augmentation_5.png" width="550">
<img src="https://github.com/OnbyshAlex/Brazilian-coin-classification/blob/master/images/augmentation_25.png" width="550">

# Result
* Custom CNN on edged images: **≈30%** accuracy
* Custom CNN on color images: **≈85%** accuracy
* Bottleneck features from VGG16: **≈97%** accuracy
* Feature tuning of VGG16: **≈98%** accuracy

Mean error for regression: **6.5** cents

