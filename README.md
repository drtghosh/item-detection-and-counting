# item-detection-and-counting
Object Detection: Counting a given item in another image

Tensorflow Object Detection API based:
Details of installation and dependencies: https://github.com/tensorflow/models/blob/master/research/object_detection/g3doc/tf1.md

Clone Tensorflow models repository to local: $ git clone https://github.com/tensorflow/models.git

Images collected from open-source data: deepcognition.ai soda-bottle challenge

Folder structure:
models\
|-annotations
 |--xmls\
     |---training\
         val\
    label_map.pbtext
|-checkpoints\
|-data\
 |--train_labels.csv
    train.record
    val_labels.csv
    val.record
|-images\
 |--training\
    val\
|-research\

Images labelled using labelImg: https://github.com/tzutalin/labelImg

Go to models/research/object_detection/samples/configs: modify the config file for ssd_mobilenet_v2_coco to change num_classes=1, train_input_reader and eval_input_reader input_path changed as per folder structure.

Train using models/research/object_detection/model_main.py
