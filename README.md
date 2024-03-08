# **Blood Cancer Detection with YOLOV5**

<img src="https://github.com/safakgunes/Blood-Cancer-Detection-YOLOV5/blob/main/yolov5/runs/train/exp/val_batch1_pred.jpg?raw=true" alt="prediction" width="600"/>

A very simple project experimenting with cancer detection (blood) using YOLOv5. 

## **Requirements**
- Anaconda 
- Poetry

## **Setting Up**
The project uses Poetry as the dependency manager and Anaconda as its runtime hence make sure Poetry is interfacing with Conda

Use the command below to install the required dependencies:
```sh
poetry install
```

## **Train**
Run commands below to start training:
```bash
poetry run python train.py --img 416 --data ../data.yaml --cfg ./models/yolov5s.yaml --batch 32 --epochs 50
```

You can see the training results and weights in the directory below at `yolov5`:

```bash
$ cd <yolov5_dir>/runs/train
```
## **Detect**

Run commands below to test:

```bash
poetry run python detect.py --source ../dataset/test/images/ --weights ./runs/train/exp/weights/best.pt --conf 0.4
```    


You can see the detection results in the `yolov5` folder:     

```bash
$ cd <yolov5_dir>/runs/detect
```
