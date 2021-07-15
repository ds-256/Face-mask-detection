# Face-mask-detection

The model stated above can detect face mask worn on a face or not by a splendid accuracy of close to 94% .

The model is a 2 stage classifier containing MTCNN for face detections as 1st stage and a Resnet head Binary classifier as the 2nd stage model.

Region proposals from the 1st staged model where face/faces are detected are passed onto the 2nd stage model which classifies whether mask is worn by surrounding bounding box with green color and for not worn by a red color.
# Outputs of the model
![alt text](https://github.com/ds-256/Face-mask-detection/blob/main/Image%20and%20video%20samples/new_onee.png)

![alt-text](https://github.com/ds-256/Face-mask-detection/blob/main/Image%20and%20video%20samples/newone.png)
