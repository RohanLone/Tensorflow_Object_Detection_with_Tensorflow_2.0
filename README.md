# Tensorflow_Object_Detection_with_Tensorflow_2.0
Soccer Player recognition using TensorFlow 2 Object Detection API With Google Colab

In this project, I used Google Colab (for model training), Google Drive (for storage) and Local machine (for model testing).
Created own dataset. Used labelimg for Annotation and saved in xml format. Converted XML to CSV using [xml_to_csv.py](https://github.com/RohanLone/Tensorflow_Object_Detection_with_Tensorflow_2.0/blob/main/xml_to_csv.py)script. 
This script(generate_tfrecords.py)[https://github.com/RohanLone/Tensorflow_Object_Detection_with_Tensorflow_2.0/blob/main/generate_tfrecord.py] will be used to covert the csv into the TFRecord format. 

I used ssd_mobilenet_v2_320x320_coco17_tpu pretrained model for training and configuration as follows:
  1. num_classes: 3
  2. fine_tune_checkpoint: "ssd_mobilenet_v2_320x320_coco17_tpu-8/checkpoint/ckpt-0"
  3. fine_tune_checkpoint_type: "detection"
  4. batch_size: 16
  5. learning_rate_base: 8e-3
  6. label_map_path: "annotations/label_map.pbtxt" (#path to your label_map file)
  7. input_path: "annotations/train.record" (#path to train.record)
  8. label_map_path: "annotations/label_map.pbtxt" (#path to your label_map file)
  9. input_path: "annotations/test.record" (#Path to test.record)


After everything successful, Loaded images with bounding boxes, labels, and accuracy! 

![alt-text](https://github.com/RohanLone/Tensorflow_Object_Detection_with_Tensorflow_2.0/blob/main/doc/7.png) 
![alt-text](https://github.com/RohanLone/Tensorflow_Object_Detection_with_Tensorflow_2.0/blob/main/doc/6.png)
![alt-text](https://github.com/RohanLone/Tensorflow_Object_Detection_with_Tensorflow_2.0/blob/main/doc/8.png)
