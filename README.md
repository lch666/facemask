# 参考项目 https://github.com/AIZOOTech/FaceMaskDetection

## [updates]
### 人脸口罩检测，现开源所有主流框架模型和推理代码，支持的框架如下：

 - [x] PyTorch
- [x] TensorFlow（包含tflite模型和pb模型）
- [x] Keras
- [x] MXNet
- [x] Caffe

## 运行方法
### pytorch
如果您要运行图片：
```
python pytorch_infer.py  --img-path /path/to/your/images   

### 新建data文件夹，MAFA数据集放data目录下
### default='./data/test_images'
### 保存目录 ./data/test.txt   pytorch_infer.py:81  pytorch_infer.py:95
### 显示图片 pytorch_infer.py:107~109
```
如果您要在视频上跑，只需要：
```
python pytorch_infer.py --img-mode 0 --video-path /path/to/video  
# 如果要打开本地摄像头, video_path填写0就可以了，如下
python pytorch_infer.py --img-mode 0 --video-path 0
```
### TensorFlow/Keras/MXNet/Caffe
另外四大框架运行方法基本类似，只不过将`pytorch_infer.py`中`pytorch`的换成`对应框架名字即可即可`，以`TensorFlow`为例：
```
python tensorflow_infer.py  --img-path /path/to/your/img
```






