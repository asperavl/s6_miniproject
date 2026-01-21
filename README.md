# PPE Detection using YOLOv8

This project trains a YOLOv8 model to detect:
- Helmet
- Vest
- Worker

Training and inference were performed using the Ultralytics YOLO CLI.

## Setup
```bash
pip install -r requirements.txt
```

## Training
```bash
yolo detect train model=yolov8n.pt data=data.yaml epochs=50
```

## Inference
```bash
yolo detect predict model=runs/detect/train/weights/best.pt source=path/to/image.jpg
```

## Notes

- YOLO treats classes independently
- PPE items may be detected even when the worker class is not detected
- Higher-level logic is required to infer compliance