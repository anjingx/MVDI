# Action recognition for depth video using multi-view dynamic images
this is the implementation of the paper accepted by Science Information

the code is consists of there pattern: 

1. multi-view dynamic images generation. 
2. multi-view CNN training.
3. faster rcnn based human motion detection 


## requirement
#### Data Download
The Dataset (such as [NTU RGBD](http://rose1.ntu.edu.sg/Datasets/actionRecognition.asp)) and the pretrained model [imagenet-vgg-f](http://www.vlfeat.org/matconvnet/pretrained/)

#### Environmet
libnear library for matlab [LIBLEANER](https://www.csie.ntu.edu.tw/~cjlin/liblinear/) is used to *generate the dynamic images.*

matconvnet-1.0-bata23 [MatConvNet](http://www.vlfeat.org/matconvnet/download/) is used for the *CNN training* stage. 

Caffe build for Faster R-CNN
  If you are using Windows, you may download a compiled mex file by running
fetch\_data/fetch\_caffe\_mex\_windows\_vs2013\_cuda65.m
## usage
#### Multi View Dynamic Images Generation
Prepare your data path then run the function file called 'MVDI_Generation/dynamic\_mutil\_general\_NTU.m'. All the involved sub-function is contained in the first folder.

#### CNN Training
After the MVDI data is generated by the former step, then feed the MVDI data to the CNN. 'View\_Shared\_CNN\_Training/train\_depth\_share\_ntu\_view_DMM/cnn\_dicnn.m' will be easy to run if your data path setting is correct.

#### Faster-RCNN based human detection 

For human detection, we construct the training sample by the human skeleton information, which described in the subfunction 'get\_bounding\_box\_skelen.m'.

'create_output.m & create\_train\_test.m' is used to create the train and test sample for training.

'script\_faster\_rcnn\_demo\_testall_ntu.m' is the final training function.
       
More detailed faster-rcnn usage can be refered to [faster_rcnn](https://github.com/ShaoqingRen/faster_rcnn).


## Citation
Please cite the following paper if you use this repository in your research.

```

	@inproceedings{
	  wew

  	  year      = {2018},
	}

```

## contact

For any question, feel free to contact

Yancheng Wang    : yancheng_wang@hust.edu.cn

Yang Xiao        ：Yang_Xiao@hust.edu.cn
