# Shelf_Detector
> Folder Structure
After cloning, organize your folders as shown below. 

    ├── Empty_Dataset
    │   ├── train
    │   ├── test
    │   └── valid
    ├── Item_Dataset
    │   ├── train
    │   ├── test
    │   └── valid
    └── Yolov5
        ├── Inputs
        ├── Outputs
        ├── Weights
        │   ├── ItemDetect.pt
        │   └── EmptyDetect.pt
        ├── models
        ├── utils
        ├── data
        ├── train.py
        └── detect.py

<br/>

[** File Download Here **](https://drive.google.com/drive/folders/1J3qiaXRBaDmvXN9wDjf3LoHP9t09bMfL?usp=sharing, "Dataset and pt File")

> Dataset
- Empty_Dataset : Supermarket Empty Shelf Detector Computer Vision Project Dataset(497) + RetailAnalysis Image Dataset(1042)
- Item_Dataset : SKU 110K Dataset (10k)

<br/>

> Train Method

    python python train.py --img 640 --batch <batch_size> --epochs <epoch> --data <data>.yaml --cfg yolov5x6.yaml --weights <pretrained model> --device <device>
    
- Optimizer : SGD
- Loss : Box Loss, Objectness Loss, Classification Loss

<br/>

> Train Result
- Empty_Dataset

    ( Pretrained by yolov5x6 )
    | Dataset        | Precision    | Recall       | mAP 50       | mAP 95       |
    | :------------: | :----------: | :-----------:| :-----------:| :-----------:|
    |  Empty_Dataset | 0.721        | 0.624        | 0.674        | 0.401        |
    |  Item_Dataset  | 0.942        | 0.894        | 0.933        | 0.75         |

<br/>

> Detect Image (TTA)

    python detect.py --augment


