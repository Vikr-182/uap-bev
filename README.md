<h1 align = "center">UAP-BEV (Uncertainty Aware Planning in Bird's Eye View) generated from Monocular Images</h1>


<p align="center">By Vikrant Dewangan<sup>1</sup>, Basant Sharma<sup>2</sup>, Sarthak Sharma<sup>1</sup>, Tushar Choudhary<sup>1</sup>, Aakash Aanegola<sup>1</sup>, 
Arun Kumar Singh<sup>2</sup>, K. Madhava Krishna<sup>1</sup></p>

<p align="center">  (1- Robotics Research Center, IIIT Hyderabad,  2- University of Tartu, Estonia)</p>

[//]: # (Paste images in this section before the table)

## Sources of Uncertainity


<table>
  <tr>
    <td><img src="/README/imgs/uncertain1.png" alt="Image 1"></td>
    <td><img src="/README/imgs/uncertain2.png" alt="Image 2"></td>
  </tr>
</table>

## Dealing with Uncertainty - Cost-Volume Approaches

![uncertain3](/README/imgs/uncertain3.png)
- Network predicts a Spatio-temporal Cost-Map.
- Trajectories indexed into the Cost Volume to choose the best trajectory.

## Dealing with Uncertainty - Parametric Assumption
![uncertain4](/README/imgs/uncertain4.png)
- Assumes shape of underlying distribution 
- Can lead to conservative behaviour
- Does not handle Noisy Annotations
- 
## We propose …. UAP-BEV
![proposal1](/README/imgs/proposal1.png)
![proposal2](/README/imgs/proposal2.png)




## Part 1: Augmenting Uncertainty into Distance Estimates
![Estimate](/README/imgs/estimate.png)

## Part 2: Efficient Batch Optimization with Constrained Projection
![proposal3](/README/imgs/proposal3.png)
![proposal4](/README/imgs/proposal4.png)
![proposal6](/README/imgs/proposal6.png)

## Scenarios Simulated



## Results

![result](/README/imgs/results.png)

## Longitudinal Barrier Ablation
![lba](/README/imgs/lba.png)

## CEM Analysis
![cem](/README/imgs/CEM.png)

**a.** **The histogram of constraint violation functions for each set in the elite set. At the start, multiple samples are spread out on non-zero values, complete convergence is achieved and at Iteration 10, all samples have values 0.**  
  
  
**b.** **Convergence of normalized costs with trace of covariance, signifying the samples are pushed towards good regions.**  






## Existing Works (Batch Optimization in Planning)




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


## Sources of Aleatoric Uncertainty
- Noise in RGB Images
- Noise in Intrinsics, error in GPS.
- Noisy BEV annotations

## Next Tasks
- Setup SIM for Cutin, Overtaking at straight, Overtaking at curved, Abrupt Stopping. Setup perspective, topdown cam.
- Setup Network. Visualize predictions on perspective, topdown cam.
- Get Future mIoU
- Integrate with MMD+RKHS, Show qualitative results.















