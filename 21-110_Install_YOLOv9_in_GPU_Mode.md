# 110. Installation: Install YOLOv9 in GPU Mode

## [YOLOv9 Repository](https://github.com/WongKinYiu/yolov9)

```shell
pip install -r requirements.txt
```

## Detection on images

```shell
python detect.py \
    --weights yolov9-c-converted.pt \
    --source data/images \
    --conf-thres 0.5 \
    --save-txt \
    --line-thickness 2
    #--view-img \
```

## Detection on image link

```shell
python detect.py \
    --weights yolov9-c-converted.pt \
    --source https://stunningvisionai.com/assets/football.png
```

## Detection on video

```shell
python detect.py \
    --weights yolov9-c-converted.pt \
    --source data/videos/road.mp4 \
    --classes 2 3 \
    --view-img
```

## Detection on webcam

```shell
python detect.py \
    --weights yolov9-c-converted.pt \
    --source 0 \
    --view-img
```