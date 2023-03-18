<h1 align = "center">UAP-BEV (Uncertainty Aware Planning in Bird's Eye View) generated from Monocular Images</h1>


<p align="center">By Vikrant Dewangan<sup>1</sup>, Basant Sharma<sup>2</sup>, Sarthak Sharma<sup>1</sup>, Tushar Choudhary<sup>1</sup>, Aakash Aanegola<sup>1</sup>, 
Arun Kumar Singh<sup>2</sup>, K. Madhava Krishna<sup>1</sup></p>

<p align="center">  (1- Robotics Research Center, IIIT Hyderabad,  2- University of Tartu, Estonia)</p>

[//]: # (Paste images in this section before the table)

## Existing Works (BEV Perception + BEV Planning)

| Paper                  | Relevance                                                |
|------------------------|----------------------------------------------------------|
| NEAT, BEVFormer, Lift-Splat, FIERY, ST-P3 | BEV monocular vision based Perception and Prediction Methods|
| NMP, P3, MP3 | BEV LiDAR based Methods. Defines the concept of Cost Volume trained on Imitation Learning cost to select a trajectory. |
| P3, ST-P3 | Defines custom costs like safety, drivable area, headway costs in BEV on top of Cost Volume cost.|


## Existing Works (Uncertainity)
| Paper                  | Relevance                                                |
|------------------------|----------------------------------------------------------|
| Kendall, Gal: WUCV, MTL | Aleatoric Uncertainty in perspective space. Does not translate into BEV. |
| Kendall: FIERY, Hu: ST-P3 |Use multi-task weight for uncertainty representation. Does not capture noisy annotations. |
| CCO-VOXEL | Use RGBD Cameras to create ESDF over Static Voxel grids. |
| Urbanfly(Closest to our work)| Use RGB + VINS-Mono pipeline to create cuboids over Static Voxel grids. Use 4 complex plane parameters to model uncertainty (height, width, rotation, yaw).|
|UoTartu (NeurIPS Workshop 2022)  (Closest to our work)| Calibration (post processing) expensive and requires . Model different types of uncertainty -object center, object shape, trajectories and requires pixel-level and object-level calibration. Does not have a planning methodology over it neither can capture noisy GT annotations. |












