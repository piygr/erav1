# Session 5 Assignment

Handwritten digits detection model based on AlexNet Architecture, trained on MNIST dataset with 60,000 images

## model.py
The file contains model class *Net* as subclass of _torch.nn.Module_. The _Net_ model is based on AlexNet architecture. 
Below is the model summary -
```
----------------------------------------------------------------
        Layer (type)               Output Shape         Param #
================================================================
            Conv2d-1           [-1, 32, 26, 26]             320
            Conv2d-2           [-1, 64, 24, 24]          18,496
            Conv2d-3          [-1, 128, 10, 10]          73,856
            Conv2d-4            [-1, 256, 8, 8]         295,168
            Linear-5                   [-1, 50]         204,850
            Linear-6                   [-1, 10]             510
================================================================
Total params: 593,200
Trainable params: 593,200
Non-trainable params: 0
----------------------------------------------------------------
Input size (MB): 0.00
Forward/backward pass size (MB): 0.67
Params size (MB): 2.26
Estimated Total Size (MB): 2.94
----------------------------------------------------------------
```

## utils.py
The file contains the generic utility functions needed to the run the model.

## S5.ipynb
The file is an IPython notebook. The notebook imports utility functions & _Net_ model class from utils.py and model.py respectively.
We are using MNIST dataset to train & test our model.
```
Adjusting learning rate of group 0 to 1.0000e-02.

Epoch 1
Train: Loss=0.4352 Batch_id=117 Accuracy=42.60: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 118/118 [03:52<00:00,  1.97s/it]
Test set: Average loss: 0.2832, Accuracy: 9150/10000 (91.50%)



Adjusting learning rate of group 0 to 1.0000e-02.

Epoch 2
Train: Loss=0.1168 Batch_id=117 Accuracy=93.40: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 118/118 [03:38<00:00,  1.85s/it]
Test set: Average loss: 0.0901, Accuracy: 9724/10000 (97.24%)



Adjusting learning rate of group 0 to 1.0000e-02.

Epoch 3
Train: Loss=0.0624 Batch_id=117 Accuracy=96.31: 100%|█████████████████████████████████████████████████████████████████████████████████████████████████████████████████████| 118/118 [03:41<00:00,  1.88s/it]
Test set: Average loss: 0.0671, Accuracy: 9781/10000 (97.81%)
```  
## How to setup
It's recommended to use virtualenv so that there's no conflict of package versions if there are multiple projects configured on a single system. Read more about [virtualenv](https://virtualenv.pypa.io/en/latest/). Once virtualenv is activatted (or otherwise), install required packages.. 

```
pip install requirements.txt
```
