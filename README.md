Object detection and instance segmentation dataset for VHR remote sensing images further marked on the NWPU VHR-10 dataset and SSDD dataset according to the standard coco dataset.

# VHR-10_dataset_coco

NWPU VHR-10 data set is a challenging ten-class geospatial object detection data set. This dataset contains a total of 800 VHR optical remote sensing images, where 715 color images were acquired from Google Earth with the spatial resolution ranging from 0.5 to 2 m, and 85 pansharpened color infrared images were acquired from Vaihingen data with a spatial resolution of 0.08 m. The data set is divided into two sets: a) Positive image set which contains at least one target in an image contains 650 images. b) Negative image set contains 150 images and it does not contain any targets. From this the positive image set, 757 airplanes, 302 ships, 655 storage tanks, 390 baseball diamonds, 524 tennis courts, 159 basketball courts, 163 ground track fields, 224 harbors, 124 bridges, and 477 vehicles were manually annotated with bounding boxes and instance masks used for ground truth.

# SSDD

The SAR ship detection dataset (SSDD) data sets include SAR images with different resolutions, polarizations, sea conditions, large sea areas, and beaches. This dataset is a benchmark for researchers to evaluate their approaches. In SSDD, there are 1160 images. For SSDD, the resolution of SAR images is as follows: 1 m, 3 m, 5 m, 7 m, and 10 m. We further mark the instance masks directly on the SSDD dataset. In this paper, we use the LabelMe open source project on GitHub to annotate these SAR images. Then, LabelMe converts the annotation message into the COCO JSON format.

### Prepare data

This code takes NWPU VHR-10 dataset as example. You can download NWPU VHR-10 dataset and put them as follows. 

```
├── show_coco.py # visualization script
├── NWPU VHR-10_dataset_coco
    ├──positive image set # 650 images
       ├── ['.jpg']
       ├──    ...
       ├── ['.jpg']
	
    ├──annotations.json # 650 labels
    ├──split_datasets.py #randomly dividing dataset scripts.
	
```
#### Dataset download link

NWPU VHR-10 dataset can be downloaded from [Google Cloud](https://drive.google.com/open?id=1--foZ3dV5OCsqXQXT84UeKtrAqc5CkAE)

SSDD dataset can be downloaded from [Google Cloud](https://drive.google.com/file/d/1grDw3zbGjQKYPjOxv9-h4WSUctoUvu1O/view?usp=sharing)


### Installation pycocotools

```
pip install pycocotools
```

### Visualization results

![image](https://github.com/chaozhong2010/VHR-10_dataset_coco/blob/master/pictures/Figure_1.png)
![image](https://github.com/chaozhong2010/VHR-10_dataset_coco/blob/master/pictures/Figure_2.png)
![image](https://github.com/chaozhong2010/VHR-10_dataset_coco/blob/master/pictures/Figure_3.png)
![image](https://github.com/chaozhong2010/VHR-10_dataset_coco/blob/master/pictures/Figure_4.png)
![image](https://github.com/chaozhong2010/VHR-10_dataset_coco/blob/master/pictures/Figure_5.png)
![image](https://github.com/chaozhong2010/VHR-10_dataset_coco/blob/master/pictures/229.png)
![image](https://github.com/chaozhong2010/VHR-10_dataset_coco/blob/master/pictures/1084.png)



### Acknowledgement

In addition, we are very grateful to NWPU for providing VHR remote sensing images. URL: [NWPU-VHR-10](http://www.escience.cn/people/gongcheng/NWPU-VHR-10.html). We also own many thanks to Jianwei Li, who generously provided the SSDD dataset.

### Citation

If you feel this dataset is useful, please cite as the following format.

[1] Su H, Wei S, Yan M, et al. Object Detection and Instance Segmentation in Remote Sensing Imagery Based on Precise Mask R-CNN[C]. IGARSS 2019-2019 IEEE International Geoscience and Remote Sensing Symposium. IEEE, 2019: 1454-1457.

[2] Su, H.; Wei, S.; Liu, S.; Liang, J.; Wang, C.; Shi, J.; Zhang, X. HQ-ISNet: High-Quality Instance Segmentation for Remote Sensing Imagery. Remote Sens. 2020, 12, 989.

