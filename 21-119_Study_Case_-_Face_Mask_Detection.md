# 21-119. Study Case: Face Mask Detection

Re-parameterize the YOLOv9 model for face mask detection using the following command:
```shell
python reparameterization.py \
    --weights runs/train/yolov9-c-face-mask/weights/best.pt \
    --variant c \
    --classes 3 \
    --output yolov9-c-face-mask-converted
```

Detect face masks in images:
```shell
python detect.py \
    --weights yolov9-c-face-mask-converted.pt \
    --source data/images/bad-mask.png \
    --view-img
```

Detect face masks in videos:
```shell
python detect.py \
    --weights yolov9-c-face-mask-converted.pt \
    --source data/videos/face-mask-video.mp4 \
    --view-img
```
