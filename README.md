# MNIST encoder-decoder
A encoder-decoder system that encode mnist(28x28)image to 16-dimension vector and decode it.
## Result

### Original image
![](./img_test.png)

### Encode-decoded image
- Test image above was encoded to 16-dimension vector.
- Then it decoded to image.
- You can see that the outline of the number is very clear but some details are removed.

![](./img_predict.png)

### Smooth change
- I picked two random image(4,9) from test dataset and encoded both of them.
- Then generate vectors between them with linear interpolation.
- Then decoded them.

![](./img_smooth_change.png)

### Random
- Decoded random vector
- They still look like some kind of number.

![](./img_random.png)

### One-Hot
- 16 image at first is decoded one-hot vector from 0 to 16.
- 17,18 is zero vector and full-one vector.
- 19 is decoded image of an encoding vector of all black image.
- You can see that there are still some white dots.
- 20 is decoded image of an encoding vector of all white image.
- You can see that the border of image is black.
- 21~24 is just black image. nothing.

![](./img_one-hot.png)


## Source code
See [MNIST-encoder.ipynb](./MNIST-encoder.ipynb) for more details.