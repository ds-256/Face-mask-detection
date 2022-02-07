# Face-mask-detection

The whole mechanism above is a 2 staged affair.
### 1st Stage

Face detection where 1 or more than 1 faces might be present in a single image is enlisted by the help of Multi task Cascaded CNN (MTCNN) state of the art model.
Model is available in both pytorch and tensorflow implementations. Pytorch one has been used because it uses GPU to it's full advantage thus resulting in large throughput.

When a single image is feed to MTCNN it outputs a single row or multi rows of vectors containing 4 column which represent the bounding box dimension in which the face or the faces have been detected.

*MTCNN also outputs the various facial landmarks but they are not used in the scope of this project.

Rectangular boxes are then drawn onto the orginal image where the face is detected by the above module.
### 2nd Stage
It is the stage which clearly demarcates whether a face mask has been worn by a person or not.

To implement that a binary classifier does a satisfactory job. This binary classifier has been trained upon 1000s and 1000s of random datasets available of images wherein some images people are wearing a mask and in others vice versa.

The Redrawn images obtained from the 1st stage are then feed onto into the binary classifer described above. Upon analysing the image the classifer prodcues a bianry output with 1 signifying that a mask is/are worn by the person/people  and 0 vice versa in that respective photo.

Thus 1 is then reinterpreted into the image with a RGB(0,0,255) vector and the converse case by RGB(255,0,0) vector.

##  Some Outputs pertaining to the Model
![alt-text](https://raw.githubusercontent.com/ds-256/Face-mask-detection/main/Image%20and%20video%20samples/nightlywork.png)

![alt-text](https://raw.githubusercontent.com/ds-256/Face-mask-detection/main/Image%20and%20video%20samples/Screenshot%20from%202021-06-26%2020-15-29.png)
