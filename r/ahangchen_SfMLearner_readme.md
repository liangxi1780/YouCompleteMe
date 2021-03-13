# SfMLearner
This codebase implements the system described in the paper:

Unsupervised Learning of Depth and Ego-Motion from Video

[Tinghui Zhou](http://u.720life.cn/g/03e37461d04d02f0b98b59fce6951e196cd8ac816f664ad3b759fed2eb1157e763d5893618de004f4ec061bee9b0d18c  [Matthew Brown](http://u.720life.cn/g/0f2c18a545db17f09ae0d75d03631a1fb80a05fa007d465893e9ad00952ecb69ebdd419634cdcaf48713e1d79d9cc1f454b74ebf9b718de92a2ff3c99639dba1  [Noah Snavely](http://u.720life.cn/g/9d81cceaad4cac689b3502cee6f35012acecb45d7e79bc8273f8d155e6767a541158e584e92481c9a974492acf5638a3  [David G. Lowe](http://u.720life.cn/g/57f1f93b56dcd457e3fcc74f0866830e6683d368ce0d5c67dde2b05637f1375ac24d3436205da1dabc938375e33933c0) 

In CVPR 2017 (**Oral**).

See the [project webpage](http://u.720life.cn/g/03e37461d04d02f0b98b59fce6951e196cd8ac816f664ad3b759fed2eb1157e72431e432e2eee75735343c02234fc96471ef34e7377df638b44b5f5b099f795b)  for more details. Please contact Tinghui Zhou (tinghuiz@berkeley.edu) if you have any questions.

 

## Prerequisites
This codebase was developed and tested with Tensorflow 1.0, CUDA 8.0 and Ubuntu 16.04.

## Running the single-view depth demo
We provide the demo code for running our single-view depth prediction model. First, download the pre-trained model by running the following
```bash
bash ./models/download_depth_model.sh
```
Then you can use the provided ipython-notebook `demo.ipynb` to run the demo.

## Preparing training data
In order to train the model using the provided code, the data needs to be formatted in a certain manner. 

For [KITTI](http://u.720life.cn/g/c98dacb123fea1f93356039236cf444a2158e28c302eeaabed8a25e405777cac32d027c1db7444830ac7e20bfc42f85662bf2b5518f356ac653d2f96079fbf3e  first download the dataset using this [script](http://u.720life.cn/g/c98dacb123fea1f93356039236cf444a336b1cf45259278add0e9907063d89091afc2bb6f379695207dfdfe6edb731370cac50bb1972f61f76f7856019405f3b)  provided on the official website, and then run the following command
```bash
python data/prepare_train_data.py --dataset_dir=/path/to/raw/kitti/dataset/ --dataset_name='kitti_raw_eigen' --dump_root=/path/to/resulting/formatted/data/ --seq_length=3 --img_width=416 --img_height=128 --num_threads=4
```
For the pose experiments, we used the KITTI odometry split, which can be downloaded [here](http://u.720life.cn/g/c98dacb123fea1f93356039236cf444a2158e28c302eeaabed8a25e405777cac4ce7825a0ab3a5b8ea4f940763f7ab139da9a95ec0f8310604247110154a419f  Then you can change `--dataset_name` option to `kitti_odom` when preparing the data.

For [Cityscapes](http://u.720life.cn/g/93d7635cef9a4049180896abf1ebad7a9867a0e59a0856e5f37ad99f8041536cafa0b5256ea67001da870a4c4ae4bca4  download the following packages: 1) `leftImg8bit_sequence_trainvaltest.zip`, 2) `camera_trainvaltest.zip`. Then run the following command
```bash
python data/prepare_train_data.py --dataset_dir=/path/to/cityscapes/dataset/ --dataset_name='cityscapes' --dump_root=/path/to/resulting/formatted/data/ --seq_length=3 --img_width=416 --img_height=171 --num_threads=4
```
Notice that for Cityscapes the `img_height` is set to 171 because we crop out the bottom part of the image that contains the car logo, and the resulting image will have height 128.

## Training
Once the data are formatted following the above instructions, you should be able to train the model by running the following command
```bash
python train.py --dataset_dir=/path/to/the/formatted/data/ --checkpoint_dir=/where/to/store/checkpoints/ --img_width=416 --img_height=128 --batch_size=4
```
You can then start a `tensorboard` session by
```bash
tensorboard --logdir=/path/to/tensorflow/log/files --port=8888
```
and visualize the training progress by opening [https://localhost:8888](http://u.720life.cn/g/5da3423f7096f513efa8032aff66538c11bb0f1331734eeb0b38d7a05f579ba8)  on your browser. If everything is set up properly, you should start seeing reasonable depth prediction after ~100K iterations when training on KITTI. 

### Notes
After adding data augmentation and removing batch normalization (along with some other minor tweaks), we have been able to train depth models better than what was originally reported in the paper even without using additional Cityscapes data or the explainability regularization. The provided pre-trained model was trained on KITTI only with smooth weight set to 0.5, and achieved the following performance on the Eigen test split (Table 1 of the paper):

| Abs Rel | Sq Rel | RMSE  | RMSE(log) | Acc.1 | Acc.2 | Acc.3 |
|---------|--------|-------|-----------|-------|-------|-------|
| 0.183   | 1.595  | 6.709 | 0.270     | 0.734 | 0.902 | 0.959 | 

When trained on 5-frame snippets, the pose model obtains the following performanace on the KITTI odometry split (Table 3 of the paper):

| Seq. 09            | Seq. 10            |
|--------------------|--------------------|
| 0.016 (std. 0.009) | 0.013 (std. 0.009) |

## Evaluation on KITTI

### Depth
We provide evaluation code for the single-view depth experiment on KITTI. First, download our predictions (~140MB) by 
```bash
bash ./kitti_eval/download_kitti_depth_predictions.sh
```
Then run
```bash
python kitti_eval/eval_depth.py --kitti_dir=/path/to/raw/kitti/dataset/ --pred_file=kitti_eval/kitti_eigen_depth_predictions.npy
```
If everything runs properly, you should get the numbers for `Ours(CS+K)` in Table 1 of the paper. To get the numbers for `Ours cap 50m (CS+K)`, set an additional flag `--max_depth=50` when executing the above command.

### Pose
We provide evaluation code for the pose estimation experiment on KITTI. First, download the predictions and ground-truth pose data by running
```bash
bash ./kitti_eval/download_kitti_pose_eval_data.sh
```
Notice that all the predictions and ground-truth are 5-frame snippets with the format of `timestamp tx ty tz qx qy qz qw` consistent with the [TUM evaluation toolkit](http://u.720life.cn/g/b09c5e123a01d72584db6b716fbdaa543dc38536be0dbb6abd0c70cc871e1883cf16786a18219b801e679dd9fd0067623722251e2ba8448f3d99df47fb6a99739e2d9edcd1d71e195c7969dd5bbd2186  Then you could run 
```bash
python kitti_eval/eval_pose.py --gtruth_dir=/directory/of/groundtruth/trajectory/files/ --pred_dir=/directory/of/predicted/trajectory/files/
```
to obtain the results reported in Table 3 of the paper. For instance, to get the results of `Ours` for `Seq. 10` you could run
```bash
python kitti_eval/eval_pose.py --gtruth_dir=kitti_eval/pose_data/ground_truth/10/ --pred_dir=kitti_eval/pose_data/ours_results/10/
```

## KITTI Testing code

### Depth
Once you have model trained, you can obtain the single-view depth predictions on the KITTI eigen test split formatted properly for evaluation by running
```bash
python test_kitti_depth.py --dataset_dir /path/to/raw/kitti/dataset/ --output_dir /path/to/output/directory --ckpt_file /path/to/pre-trained/model/file/
```
Again, a sample model can be downloaded by
```bash
bash ./models/download_depth_model.sh
```

### Pose
We also provide sample testing code for obtaining pose predictions on the KITTI dataset with a pre-trained model. You can obtain the predictions formatted as above for pose evaluation by running
```bash
python test_kitti_pose.py --test_seq [sequence_id] --dataset_dir /path/to/KITTI/odometry/set/ --output_dir /path/to/output/directory/ --ckpt_file /path/to/pre-trained/model/file/
```
A sample model trained on 5-frame snippets can be downloaded by
```bash
bash ./models/download_pose_model.sh
```
Then you can obtain predictions on, say `Seq. 9`, by running
```bash
python test_kitti_pose.py --test_seq 9 --dataset_dir /path/to/KITTI/odometry/set/ --output_dir /path/to/output/directory/ --ckpt_file models/model-100280
```

## Other implementations
[Pytorch](http://u.720life.cn/g/54145d0471d91890860f7f8463c030461d9bd69290e3e08721631c6b6775f48219f1e9bfe6ed0c93497d7971b83397aae1623d668c6c9064c7f6c2f515c18139)  (by Clement Pinard)

## Disclaimer
This is the authors' implementation of the system described in the paper and not an official Google product.



 # 良心友情链接

[腾讯QQ群快速检索](http://u.720life.cn/s/8cf73f7c)

[软件免费开发论坛](http://u.720life.cn/s/bbb01dc0)