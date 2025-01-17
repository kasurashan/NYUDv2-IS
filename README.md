# NYUDv2-IS
A dataset converted from NYUDv2 into COCO-style instance segmentation format \
For detailed statistics about our dataset, please refer to the following paper:\
**[IAM: Enhancing RGB-D Instance Segmentation with New Benchmarks](https://arxiv.org/abs/2501.01685)** 
![image](./img/img1.jpg)

```
Train   : 795 images
Val     : 654 images
Classes : 9
Size    : 640 × 480
Sensor  : Kinect V1
```

## Data preparation

NYUDv2 : https://huggingface.co/datasets/kasurashan/RGBD-Instance-Segmentation

```
NYUDv2/
└── train/
    └── color/
└── val/
    └── color/
└── annotations/
    └── instances_train.json
    └── instances_val.json
└── depth/
└── hha/
```

## Data Format
```
annotation{
    "id": int,
    "image_id": int,
    "category_id": int,
    "segmentation": [polygon],
    "area": float,
    "bbox": [x,y,width,height],
    "iscrowd": 0 or 1,
}

categories[{
    "id": int,
    "name": str,
    "supercategory": str,
}]
```
