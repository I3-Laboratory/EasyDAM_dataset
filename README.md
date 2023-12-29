## EasyDAM_dataset
The dataset is used in the paper "EasyDAM_V4: Guided-GAN based cross-species data labeling for fruit detection with significant shape difference".  (in Press) 
## Dataset and Pretrained models available here:
Please fill out [this form](https://forms.gle/PFhxjcpQZvq3xvo46) to get the download link.  

We also provide examples of automatic labeling images as follows.  

<img src="https://github.com/I3-Laboratory/EasyDAM_dataset/blob/main/test_picture.jpg" width="400px">  

## Install
 Clone this repo:  
```
git clone https://github.com/I3-Laboratory/EasyDAM_dataset
```  
 Create a new conda environment and activate the environment.
```
conda create --name EasyDAM_V4 python=3.6
conda activate EasyDAM_V4
```
 Install the requirements.  
```
conda install pytorch=0.4.1 torchvision -c pytorch
git clone https://github.com/cocodataset/cocoapi.git $COCOAPI
cd $COCOAPI/PythonAPI  
make  
python setup.py install --user
pip install -r requirements.txt
cd $CenterNet_ROOT/src/lib/models/networks/DCNv2  
./make.sh  
```
