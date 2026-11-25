# 21-123 Vehicle Counter Project Part 3: Speed Estimation

```shell
python speed_estimation.py \
    --weights yolov9-c-converted.pt \
    --video data/videos/highway.mp4
```

For video files, speed is calculated from the video's frame timestamps, not
from the computer's processing time. The perspective region and the
`distance / 10` conversion in `speed_estimation.py` are scene calibration
values and must match the camera view.