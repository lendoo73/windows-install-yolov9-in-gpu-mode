# 21-120. Accuracy Measurement using Mean Average Precision

Calculating MAP on the validation dataset:
```shell
python val.py \
    --data data/face_mask.yaml \
    --weights yolov9-c-face-mask-converted.pt \
    --batch-size 2 \
    --conf-thres 0.001 \
    --iou-thres 0.5 \
    --device 0 \
    --name yolov9-c-face-mask-val \
    --task val
```

Calculating MAP on the test dataset:
```shell
python val.py \
    --data data/face_mask.yaml \
    --weights yolov9-c-face-mask-converted.pt \
    --batch-size 2 \
    --conf-thres 0.001 \
    --iou-thres 0.5 \
    --device 0 \
    --name yolov9-c-face-mask-test \
    --task test
```