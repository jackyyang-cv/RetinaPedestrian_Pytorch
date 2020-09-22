

##### Data
1. Download CityPersons  coco2014 CrowdHuman CUHKocclusion ETHZ VOCdevkit  dataset to train.

2. convert  annotations as follow:
   retina-train.txt
   content:
   # G:\datasets\pedestrian\CityPersons\images\train\aachen_000000_000019_leftImg8bit.png
   892 445 913 498  #lefttop point  right bottom point
   901 443 935 498
   1844 436 1888 542
   # G:\datasets\pedestrian\CityPersons\images\train\aachen_000002_000019_leftImg8bit.png
   1290 425 1315 486

## Train
$ train.py [-h] [data_path DATA_PATH] [--batch BATCH]
                [--epochs EPOCHS]
                [--shuffle SHUFFLE] [img_size IMG_SIZE]
                [--verbose VERBOSE] [--save_step SAVE_STEP]
                [--eval_step EVAL_STEP]
                [--save_path SAVE_PATH]
                [--depth DEPTH]

#### Example
For multi-gpus training, run:

$ CUDA_VISIBLE_DEVICES=0,1,2,3 python3 train.py 

#### Training log
missing  due to other reason


##### Result:
the improvement of AP is little compare to face detect. the reason maybe:
1. the sample has more mistake in label. so focal loss will learn more bad thing.
2. pedestrian box has more background and shield. the detection is more difficult.
## Todo: 
- [ ] 

refrence:
https://github.com/supernotman/RetinaFace_Pytorch.git