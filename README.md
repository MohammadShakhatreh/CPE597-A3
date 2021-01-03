# Assignment #4

In this assignment I used SVM using two different kernels which are the linear and the gaussian kernels.

## Linear Kernel

I started to test different values of `C` to see what 
value gives me the best results, I have tested values in [0.01, 10] range with an increament value of 0.01 using cross validation dataset.

The best value of `C` was 0.02 which gives an f1 score of 0.658.

## Gaussian Kernel

In this kernel I needed to find two values `C` and `Gamma`, for `C` I have tested [1, 10] range with an increament of 1, and for `Gamma` I have tested [80, 100] with an increament of 0.1 using cross validation dataset.

This gave me `C=1` and `Gamma=80.5` which give the an f1 score of 1 on the training and validtion datasets and a score of 0.984 for the testing dataset.

## Conclusions

- I didn't use features scaling because the dataset is already scaled between 0 and 1 for both features.
- Linear kernel didn't give good results in comparison to the gaussian kernel because the dataset can't be separated using a single linear line.
- Cross validation dataset helped me to find the best parameters for both kernels and using the default parameters of the SVM library wouldn't give me good results.