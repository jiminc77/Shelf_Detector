# Shelf_Detector
> Folder Structure <br/>

After cloning, organize your folders as shown below

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



[ File Download Here ](https://drive.google.com/drive/folders/1J3qiaXRBaDmvXN9wDjf3LoHP9t09bMfL?usp=sharing, "Dataset and pt File")

<br/>

> Dataset
- Empty_Dataset : Supermarket Empty Shelf Detector Computer Vision Project Dataset(497) + RetailAnalysis Image Dataset(1042)
- Item_Dataset : SKU 110K Dataset (10k)

<br/>

> Train Method

<br/>
Install

    git clone https://github.com/jiminc77/Shelf_Detector.git  # clone
    cd yolov5
    pip install -r requirements.txt  # install

Training

    python python train.py --img 640 --batch <batch_size> --epochs <epoch> --data <data>.yaml --cfg yolov5x6.yaml --weights <pretrained model> --device <device>
    
- Optimizer : SGD
- Loss : Box Loss, Objectness Loss, Classification Loss

<br/>

> Train Result
- Empty_Dataset

    ( Pretrained by yolov5x6 )
    | Dataset        | Precision    | Recall       | mAP<sup>val<br>50 | mAP<sup>val<br>95 |
    | :------------: | :----------: | :-----------:| :-----------:| :-----------:|
    |  Empty_Dataset | 0.721        | 0.624        | 0.674        | 0.401        |
    |  Item_Dataset  | 0.942        | 0.894        | 0.933        | 0.75         |

<br/>

> Detect Image (TTA)

    python detect.py --augment


![IMG_5359](https://github.com/jiminc77/Shelf_Detector/assets/91927189/f5e0a5ff-8e93-4607-aefe-b379cd833ab7)
![IMG_5393](https://github.com/jiminc77/Shelf_Detector/assets/91927189/ba39a2b6-a505-4540-8207-d8ed9b46c593)


