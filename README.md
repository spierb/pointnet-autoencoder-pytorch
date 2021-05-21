# pointnet-autoencoder-pytorch

Pytorch implementation of PointNet-AutoEncoder.

Implementation is on **python3.6**, **pytorch1.8.1**. And **open3d** is required to display the pointcloud.

Paper:https://openaccess.thecvf.com/content_cvpr_2017/papers/Qi_PointNet_Deep_Learning_CVPR_2017_paper.pdf

![image](https://user-images.githubusercontent.com/44312407/119113376-a1898f00-ba57-11eb-96ea-de4872c24194.png)

---

## Result
Training loss:

![image](https://user-images.githubusercontent.com/44312407/119115840-33929700-ba5a-11eb-87e3-379a623f66f6.png)

Reconstruction of Airplane point cloud, red pcd is the ground truth and the green one is the reconstructed point cloud.

![image](https://user-images.githubusercontent.com/44312407/119115923-4b6a1b00-ba5a-11eb-9096-abd6647bc56a.png)

Reconstruction of Chair point cloud.

![569262122](https://user-images.githubusercontent.com/44312407/119116294-af8cdf00-ba5a-11eb-8c4e-0d5e18de3483.jpg)


## Data

Download the [ShapeNet dataset](https://shapenet.cs.stanford.edu/media/shapenetcore_partanno_segmentation_benchmark_v0.zip), unzip and move the **shapenetcore_partanno_segmentation_benchmark_v0** folder to the workspace dir.

## Train

Using ```python train.py -h``` for more options.

Example for training on Chair category:
```
python train.py --category Chair --log_dir ${path_to_your_log_directory}
```

## Test
Using ```python test.py -h``` for more options.

Example for testing on Chair category:
```
python test.py --model {path_to_model.pth} --category Chair
```
