# Behavioural-Cloning-of-Self-Driving-Car
Towards a trend in bridging the gap of building the Self-Driving vehicles using Convolutional Neural Networks, cloning the behavior of a trained vehicle data onto another platform could be a challenging task to deal with random obstacles like biased nature in data. The most general case could be observed when training the vehicle on a one way circular track and transfer that knowledge to a vehicle on different track. In this project, NVidia model of Convolutional Neural Networks is used to train the car with required Data Augmentation techniques to reduce the influence of biased data in detecting the steering angle of the Vehicle. The initial training to the car in a circular track of simulator has been given in clockwise, anticlockwise directions. The error prone zones are analyzed and provided more information with different image manipulation techniques. Transferred knowledge of the generalized trained data has been tested on a different track in the simulator with required augmentation techniques induced.


Summary of the First Model
The following is the summary of the first network, without the dropout layers and with the learning rate of 0.01. Note that this model was tested before on not augmented data set.
_________________________________________________________________
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_1 (Conv2D)            (None, 31, 98, 24)        1824      
_________________________________________________________________
conv2d_2 (Conv2D)            (None, 14, 47, 36)        21636     
_________________________________________________________________
conv2d_3 (Conv2D)            (None, 5, 22, 48)         43248     
_________________________________________________________________
conv2d_4 (Conv2D)            (None, 3, 20, 64)         27712     
_________________________________________________________________
conv2d_5 (Conv2D)            (None, 1, 18, 64)         36928     
_________________________________________________________________
flatten_1 (Flatten)          (None, 1152)              0         
_________________________________________________________________
dense_1 (Dense)              (None, 100)               115300    
_________________________________________________________________
dense_2 (Dense)              (None, 50)                5050      
_________________________________________________________________
dense_3 (Dense)              (None, 10)                510       
_________________________________________________________________
dense_4 (Dense)              (None, 1)                 11        
_________________________________________________________________
Total params: 252,219
Trainable params: 252,219
Non-trainable params: 0


Summary of the Final Model
The following is the summary for the final model.
Layer (type)                 Output Shape              Param #   
=================================================================
conv2d_6 (Conv2D)            (None, 31, 98, 24)        1824      
_________________________________________________________________
conv2d_7 (Conv2D)            (None, 14, 47, 36)        21636     
_________________________________________________________________
conv2d_8 (Conv2D)            (None, 5, 22, 48)         43248     
_________________________________________________________________
conv2d_9 (Conv2D)            (None, 3, 20, 64)         27712     
_________________________________________________________________
conv2d_10 (Conv2D)           (None, 1, 18, 64)         36928     
_________________________________________________________________
flatten_2 (Flatten)          (None, 1152)              0         
_________________________________________________________________
dense_5 (Dense)              (None, 100)               115300    
_________________________________________________________________
dropout_4 (Dropout)          (None, 100)               0         
_________________________________________________________________
dense_6 (Dense)              (None, 50)                5050      
_________________________________________________________________
dropout_5 (Dropout)          (None, 50)                0         
_________________________________________________________________
dense_7 (Dense)              (None, 10)                510       
_________________________________________________________________
dropout_6 (Dropout)          (None, 10)                0         
_________________________________________________________________
dense_8 (Dense)              (None, 1)                 11        
_________________________________________________________________
Total params: 252,219
Trainable params: 252,219
Non-trainable params: 0
