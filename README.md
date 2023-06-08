# Shelf_Detector
> Folder Structure <br/>

After cloning and downloading dataset, organize your folders as shown below

[ Dataset Download Here ](https://drive.google.com/drive/folders/1J3qiaXRBaDmvXN9wDjf3LoHP9t09bMfL?usp=sharing, "Dataset and pt File")

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
        │   ├── ItemDetect.engine
        │   └── EmptyDetect.engine
        ├── models
        ├── utils
        ├── data
        ├── train.py
        ├── yolov5x6.pt
        └── detect.py




<br/>

> Dataset
- Empty_Dataset : Supermarket Empty Shelf Detector Computer Vision Project Dataset(497) + RetailAnalysis Image Dataset(1042)
- Item_Dataset : SKU 110K Dataset (10k)

<br/>

> Train Method

Install

    git clone https://github.com/jiminc77/Shelf_Detector.git  # clone
    cd Shelf_Detector/Yolov5
    pip install -r requirements.txt  # install

Training

    python train.py --img 640 --batch <batch_size> --epochs <epoch> --data <ItemDetect or EmptyDetect>.yaml --cfg yolov5x6.yaml --weights <yolov5x6.pt> --device <device>
    
- Optimizer : SGD
- Loss : Box Loss, Objectness Loss, Classification Loss

<br/>

> Train Result
- Empty_Dataset

    ( Pretrained by yolov5x6 )
    | Dataset        | Precision    | Recall       | mAP<sup>val<br>50 | mAP<sup>val<br>95 |
    | :------------: | :----------: | :-----------:| :-----------:| :-----------:|
    |  Empty_Dataset | 0.731        | 0.646        | 0.723        | 0.414        |
    |  Item_Dataset  | 0.942        | 0.894        | 0.933        | 0.75         |

<br/>

> Detect Image (TTA)

    python detect.py --augment


![IMG_5359](https://github.com/jiminc77/Shelf_Detector/assets/91927189/f5e0a5ff-8e93-4607-aefe-b379cd833ab7)
![IMG_5393](https://github.com/jiminc77/Shelf_Detector/assets/91927189/ba39a2b6-a505-4540-8207-d8ed9b46c593)


