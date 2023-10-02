# Webblood
## Download yolov7 
```git
git clone https://github.com/WongKinYiu/yolov7.git
```
After downloading
```
pip install -r requirements.txt
```
## Split the dataSet into 80-20

Make data.yaml file in data
```
train: ./dataSet1/Train/
val : ./dataSet1/Test/

nc: 1
name: ["Cells"]
```
## Download yolov7.pt weight from YOLOv7 doc
```
wget https://github.com/WongKinYiu/yolov7/releases/download/v0.1/yolov7.pt
```

## Training commands
```
python train.py --workers 8 --device 0 --batch-size 32 --data data/data.yaml --img 640 640 --cfg cfg/training/yolov7.yaml --weights yolov7.pt --name yolov7 --hyp data/hyp.scratch.p5.yaml --epochs 100
```

Resource
```
https://blog.paperspace.com/train-yolov7-custom-data/
```



