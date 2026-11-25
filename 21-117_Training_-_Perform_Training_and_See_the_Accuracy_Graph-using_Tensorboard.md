# 21-117. Training: Perform Training and See the Accuracy Graph using Tensorboard

[YOLOv9 Repository](https://github.com/WongKinYiu/yolov9)

Training command for face mask detection using YOLOv9:

```shell
python train_dual.py \
    --weights yolov9-c.pt \
    --data data/face_mask.yaml \
    --img 640 \
    --device 0 \
    --workers 0 \
    --batch-size 2 \
    --cfg models/detect/yolov9-c.yaml \
    --hyp data/hyps/hyp.scratch-high.yaml \
    --epochs 100 \
    --patience 50 \
    --name yolov9-c-face-mask
```

See the accuracy graph using Tensorboard:

```shell
tensorboard --logdir=runs/train/yolov9-c-face-mask
```

Continue training:

```shell
python train_dual.py \
    --weights runs/train/yolov9-c-face-mask/weights/last.pt \
    --resume
```