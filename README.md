# Shelf_Detector
> Folder Structure


    ├── Empty_Dataset
    │   ├── train
    │   ├── test
    │   └── valid
    ├── Item_Dataset
    │   ├── train
    │   ├── test
    │   └── valid
    ├── Yolov5
    │   ├── train.py
    │   └── detect.py
    └── run.sh

    [File Download Here](https://drive.google.com/drive/folders/1J3qiaXRBaDmvXN9wDjf3LoHP9t09bMfL?usp=sharing, "Dataset and pt File")

> Dataset
- Empty_Dataset : Supermarket Empty Shelf Detector Computer Vision Project Dataset(497) + RetailAnalysis Image Dataset(1042)
- Item_Dataset : SKU 110K Dataset (10k)

> Train Result
- Empty_Dataset

    ( Pretrained by yolov5x6 )
    | Dataset        | Precision    | Recall       | mAP 50       | mAP 95       |
    | :------------: | :----------: | :-----------:| :-----------:| :-----------:|
    |  Empty_Dataset | 0.721        | 0.624        | 0.674        | 0.401        |
    |  Item_Dataset  | 0.942        | 0.894        | 0.933        | 0.75         |

     
