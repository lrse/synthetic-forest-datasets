# Synthetic Forest Datasets
Synthetic Forest Datasets created by LRSE-Fortest-Simulator.

We present two datasets: A LiDAR-like dataset, that consists of the point cloud of several scenes extracted from the LRSE Forest Simulator, and a camera-like dataset, that also consists of the point cloud of several scenes extracted from the same simulator, but processed to add occlusion from a top-down view, using Katz, S., et. al.: Direct visibility of point sets. 

## LiDAR-like Dataset

Link: https://1drv.ms/u/s!ArbJQwj1LF0AuRZMVaHYouwmcvyZ?e=eqbrjA 

For repitability, the seed used to generate the datasets are: 03, 08, 11, 48, 76, 85.

## Camera-like Dataset

Link: https://1drv.ms/u/s!ArbJQwj1LF0AuRVK3oMfYmz3LEtd?e=vqYo4G 

For repitability, the seed used to generate the datasets are: 03, 05, 08, 11, 15, 22, 27, 32, 36, 43, 48, 54, 60, 69, 72, 76, 85, 87, 91, 93.

## Format
The format of the dataset is given taking the ShapeNetPart dataset format as an example. In both cases the files are distributed as 75% for training, 15% for validation and 15% for testing.

Both Datasets counts with the following format: **x, y, z, category**
where **x, y, z** represents the space coordinates of the point, and **category** is set as:
 - 0 : Terrain points
 - 1 : Trunk points
 - 2 : Canopy points
 - 3 : Understorey, including bushes, grass and other vegetation

The files are named taken the following convention: a_n_m.txt, where a stands for the number of the scene, n stands for is n-th division of the scene, and m stands for the m-th subcloud of the n-th partition. Each of the n partitions have a maximum of 2500000 points, whereas each subcloud has approximately 10000 points from that partition, segmented in the xy plane using K-means. 

## Forest Simulator Configuration
In the annexed SilatorConfiguration file there are presented the parameters used in the simulator to generate both datasets. 

## Reference
This dataset was publish in the paper:
Raverta Capua F., Schandin J., De Cristóforis, P.: Training point-based deep learning networks for forest segmentation with synthetic data. Presented to the ICPR 2024, publicly available in arxiv. 