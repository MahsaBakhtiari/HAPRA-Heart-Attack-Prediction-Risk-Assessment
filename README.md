# Heart AI


## ECG Image Classification
### An overview of Electrocardiogram (ECG or EKG) 
![](https://www.mayoclinic.org/-/media/kcms/gbs/patient-consumer/images/2016/10/11/18/07/mcdc7_electrocardiogram-8col.jpg)

*An electrocardiogram records the electrical signals in the heart. It's a common and painless test used to detect heart problems and monitor the heart's health quickly.*

It's used  to determine or detect:
* Irregular heart rhythms (arrhythmias)
* If blocked or narrowed arteries in the heart (coronary artery disease) are causing chest pain or a heart attack
* Whether you have had a previous heart attack
* How well certain heart disease treatments, such as a pacemaker, are working
### Identifying heart defects from ECG Images with Deep Learning
As discussed before, ECGs are one of the main sensory methods used by physicians to identify heart problems. In this project we use a dataset of already annotated ECG records stored as images and their corresponding heart disease labels generated by doctors to train a ViT (Vision Transformer) model to identify different heart conditions based on the input ECG image. The dataset contains ECG images for the following conditons:

* Normal Heart
* Myocardial Infarction
* Abnormal Heart Beat
* Have a History of Myocardial Infraction

#### Data Preprocessing
The original images have a resolution of 2213 x 1572. This resolution is very inefficient for deep learning processing as it quickly fills the precious GPU memory with large feature maps. In order to make the problem practical, I downsapled the images to a resolution of 182 x 256 to keep their original aspect ratio. It is important to use the correct downsampling algorithm so that the ECG lines are still visible and their tiny fluctuations are not destroyed. For this purpose I visually inspected the down sampled images and the "area" interpolation approach yielded the best results.

## Resources
* https://data.mendeley.com/datasets/gwbz3fsgp8/2
* https://www.kaggle.com/datasets/iamsouravbanerjee/heart-attack-prediction-dataset/

