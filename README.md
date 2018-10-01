# Are-You-Happy
CNN model to detect if the person in the input image is happy or not. It is implemented in Keras.

## The model in a nutshell

```python
      INPUT
      -> | zero_padding((3, 3)) -> conv2D(32, (7, 7)) -> batchNorm -> relu -> maxPool((2, 2)) | 
      -> | zero_padding((2, 2)) -> conv2D(64, (5, 5)) -> batchNorm -> relu -> maxPool((2, 2)) |
      -> | zero_padding((1, 1)) -> conv2D(128, (3, 3)) -> batchNorm -> relu -> maxPool((2, 2)) |
      -> | conv2D(64, (1, 1)) -> batchNorm -> relu |
      -> | zero_padding((1, 1)) -> conv2D(32, (3, 3)) -> batchNorm -> relu -> maxPool((2, 2)) |
      -> | Flatten -> dense_layer_1(128, sigmoid) -> dense_layer_2(32, sigmoid) -> dense_layer_3(1, sigmoid) |
      -> OUTPUT
```

## Finally to play around with the model

The "is_it_happy_face" function implemented takes the prediction matrix, the correspnding matrix containing the RGB values and the index that we want to check for.


![oooo](https://user-images.githubusercontent.com/38986305/46318240-71192c00-c5f3-11e8-9f60-d2cd829fe356.JPG)
![pppppp](https://user-images.githubusercontent.com/38986305/46318242-71192c00-c5f3-11e8-8708-161a4a11f95d.JPG)
