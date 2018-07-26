# OpenVino SRCNN
## 0.Introduction

This model is developed by Department of Informaiton Engineering, The Chinese University of Hong Kong and Microsoft Research.
Original Author: Chao Dong, Chen Change Loy, Kaiming He, Xiaoou Tang.

This repo contains the Intel OpenVino implementation of this model.

Project Page: 
http://mmlab.ie.cuhk.edu.hk/projects/SRCNN.html

Github repo: 
https://github.com/WangDequan/SRCNN#srcnn

Caffe Model: 
https://github.com/Joyce511/OpenVino_SRCNN/blob/master/SRCNN/SRCNN_iter_11112465.caffemodel
Prototxt:
https://github.com/Joyce511/OpenVino_SRCNN/blob/master/SRCNN/SRCNN.prototxt


## 1.Prerequisite
- Intel OpenVino Toolkit 2018 R2
- Jupyter Notebook
- Open CV2
- Python 3.5 or higher
- Numpy
- Matplotlib
- clDNN for GPU mode

## 2. Usage

```
$ git clone https://github.com/Joyce511/OpenVino_SRCNN.git
$ cd OpenVino_SRCNN/SRCNN
$ jupyter notebook 
```
- In jupyter notebook, click to open SRCNN_OpenVino_Video_CPU.ipynb / SRCNN_OpenVino_Video_GPU.ipynb
- On the upper handlebar, click Cell > Run All

## 3. Performance
### Single-image performance

#### Test image
![alt text](https://github.com/Joyce511/OpenVino_SRCNN/blob/master/SRCNN/Test/Set14/face_2.bmp)
#### Image size
- 500x658 px
#### Performance
- OpenVino w/ converted .xml model: ~40ms
- Caffe w/ original .caffemodel model: ~800ms

- For further comparison, refer to SRCNN_Caffe_single_image.ipynb and SRCNN_OpenVino_single_image.ipynb

### Video-input performance
#### Video size
- 320x240
#### Performance
- OpenVino w/ converted .xml mode, CPU model: ~ 20 frame/sec
- Caffe w/ original .caffemodel model: ~ 1.5 frame/sec

- For further comparasion, refer to SRCNN_Caffe_Video.ipynb and SRCNN_OpenVino_Video_CPU.ipynb

## 4.Sample Results
![alt text](https://github.com/Joyce511/OpenVino_SRCNN/blob/master/results/result1.png)
![alt text](https://github.com/Joyce511/OpenVino_SRCNN/blob/master/results/result2.png)

