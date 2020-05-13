### [Kaggle Bengali Challenge](https://www.kaggle.com/c/bengaliai-cv19)

My solution to computer vision Bengali challenge  
  
Preprocessing includes centering image to the region of interest based on pixel values, resizing to 128x128 size and normalizing pixel values.  
I had some OOM issues trying to submit prediction, so I had to divide test dataset into several parts to save memory.  
  
For image augmentation:   
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ rotation_range=5,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ zoom_range = 0.1,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ width_shift_range=0.1,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ height_shift_range=0.1,  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;+ mix_up_alpha = 0.4)  

There is a custom Image Data Generator to include mixup, since original tensorflow ImageDataGenerator class doesnt have that augmentation.  
For model I chose to build my own CNN model, since I wanted to see the ouctome of different structures, hyperparameters etc.

**What didn't work:**  
&nbsp;&nbsp;Cutout and cutmix augmentations  
&nbsp;&nbsp;Class weights  
&nbsp;&nbsp;L1 or L2 regularization  
&nbsp;&nbsp;Per-pixel or per-image subtraction
