# YoloV5-Tensorflow2.X
 
Dataset URL:https://mega.nz/file/d5s2HYwJ#VfwoKiAUFs38zwgYpDY4w87hNl0Iqi8goQGGffXop0I
-------------
Object Detection model weights URL:https://mega.nz/file/MmpDTB6L#622wYRl9DyUpZkSM8xQzSrV1KPMidQ8KzL_8SBQzlNQ
-------------

<div align="center">
<img src="https://github.com/Wade0125Studio/YoloV5-Tensorflow2.X/blob/main/img/street.jpg">
</div>

<div align="center">
<img src="https://github.com/Wade0125Studio/YoloV5-Tensorflow2.X/blob/main/img_out/street.png">
</div>

------------
#Video Demo URL:https://youtu.be/zi1RnSC2R7I
------------

<p align="center" >Indicator performance</font></p>

<div align="center">
<img src="https://github.com/Wade0125Studio/YoloV5-Tensorflow2.X/blob/main/map_out/results/mAP.png">
</div>

<div align="center">
<img src="https://github.com/Wade0125Studio/YoloV5-Tensorflow2.X/blob/main/map_out/results/lamr.png">
</div>

<div align="center">
<img src="https://github.com/Wade0125Studio/YoloV5-Tensorflow2.X/blob/main/map_out/results/ground-truth-info.png">
</div>

------------
## Evaluation steps
### a. Test set for evaluating VOC07+12
1. This paper uses the VOC format for evaluation. VOC07+12 has already divided the test set, there is no need to use voc_annotation.py to generate the txt under the ImageSets folder.
2. Modify model_path and classes_path in yolo.py. **model_path points to the trained weights file in the logs folder. classes_path points to the txt corresponding to the detection category. **
3. Run get_map.py to get the evaluation result, which will be saved in the map_out folder.

### b. Evaluate your own dataset
1. This paper uses the VOC format for evaluation.
2. If the voc_annotation.py file has been run before training, the code will automatically divide the data set into training set, validation set and test set. If you want to modify the proportion of the test set, you can modify the trainval_percent in the voc_annotation.py file. trainval_percent is used to specify the ratio of (training set + validation set) to test set, by default (training set + validation set): test set = 9:1. train_percent is used to specify the ratio of training set to validation set in (training set + validation set), by default training set:validation set = 9:1.
3. After dividing the test set with voc_annotation.py, go to the get_map.py file to modify the classes_path. The classes_path is used to point to the txt corresponding to the detection category. This txt is the same as the txt during training. Evaluating your own datasets must be modified.
4. Modify model_path and classes_path in yolo.py. **model_path points to the trained weights file in the logs folder. classes_path points to the txt corresponding to the detection category. **
5. Run get_map.py to get the evaluation result, which will be saved in the map_out folder.

## Reference
https://github.com/qqwweee/keras-yolo3/  
https://github.com/Cartucho/mAP  
https://github.com/Ma-Dan/keras-yolo4  
https://github.com/ultralytics/yolov5







