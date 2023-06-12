# Gesture recognition
Gesture recognition using Keras
## Environment 
* Jupyter notebook in Windows 10
* Using CPU
* Python 3.11
* TensorFlow v2.12.0
## About dataset
It has 10 classes of gesture：
* palm
* letter "L"
* fist
* fist_moved
* thumb
* index
* ok
* palm_moved
* letter "C"
* down
## Model
```
_________________________________________________________________
 Layer (type)                Output Shape              Param #   
=================================================================
 conv2d (Conv2D)             (None, 240, 640, 32)      2432      
                                                                 
 max_pooling2d (MaxPooling2D  (None, 120, 320, 32)     0         
 )                                                               
                                                                 
 conv2d_1 (Conv2D)           (None, 118, 318, 32)      9248      
                                                                 
 max_pooling2d_1 (MaxPooling  (None, 59, 159, 32)      0         
 2D)                                                             
                                                                 
 conv2d_2 (Conv2D)           (None, 57, 157, 64)       18496     
                                                                 
 conv2d_3 (Conv2D)           (None, 55, 155, 64)       36928     
                                                                 
 conv2d_4 (Conv2D)           (None, 53, 153, 128)      73856     
                                                                 
 max_pooling2d_2 (MaxPooling  (None, 26, 76, 128)      0         
 2D)                                                             
                                                                 
 global_average_pooling2d (G  (None, 128)              0         
 lobalAveragePooling2D)                                          
                                                                 
 dropout (Dropout)           (None, 128)               0         
                                                                 
 flatten (Flatten)           (None, 128)               0         
                                                                 
 activation (Activation)     (None, 128)               0         
                                                                 
 dense (Dense)               (None, 10)                1290      
                                                                 
 activation_1 (Activation)   (None, 10)                0         
                                                                 
=================================================================
Total params: 142,250
Trainable params: 142,250
Non-trainable params: 0
_________________________________________________________________
```
## Accuracy
Accuracy of the model：80.85%
