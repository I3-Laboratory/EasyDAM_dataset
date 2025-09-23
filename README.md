## EasyDAM_dataset  
The dataset is used in the paper:  
Wenli Zhang, Yuxin Liu, Chenhuizi Wang, Chao Zheng, Guoqiang Cui, Wei Guo, EasyDAM_V4: Guided-GAN-based cross-species data labeling for fruit detection with significant shape difference, Horticulture Research, Volume 11, Issue 3, March 2024, uhae007, https://doi.org/10.1093/hr/uhae007

## Dataset and Pretrained models available here:
Please fill out [this form](https://forms.gle/PFhxjcpQZvq3xvo46) to get the download link.  

We also provide examples of automatic labeling images as follows.  

<img src="https://github.com/I3-Laboratory/EasyDAM_dataset/blob/main/test_picture.jpg" width="400px">  

## Install
 Clone this repo.  
```
git clone https://github.com/I3-Laboratory/EasyDAM_dataset
```  
 Create a new conda environment and activate the environment.
```
conda create --name EasyDAM_V4 python=3.6
conda activate EasyDAM_V4
```
 Install pytorch 0.4.1 and COCOAPI. 
```
conda install pytorch=0.4.1 torchvision -c pytorch
git clone https://github.com/cocodataset/cocoapi.git $COCOAPI
cd $COCOAPI/PythonAPI  
make  
python setup.py install --user   
```
 Install the requirements.  
```
pip install -r requirements.txt
```
 Compile deformable convolutional (from DCNv2).  
```
cd $EasyDAM_dataset/CenterNet/src/lib/models/networks/DCNv2  
./make.sh
```
## Usage
We support demo for automatic labeling.  

First, download the pretrained models and put them in EasyDAM_dataset/CenterNet/exp/.  

Then, run:  
```
python demo.py ctdet --demo /path/to/image --load_model ../models/ctdet_coco_dla_2x.pth
```
