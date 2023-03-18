<h1 align = "center">UAP-BEV (Uncertainty Aware Planning in Bird's Eye View) generated from Monocular Images</h1>


<p align="center">By Vikrant Dewangan<sup>1</sup>, Basant Sharma<sup>2</sup>, Sarthak Sharma<sup>1</sup>, Tushar Choudhary<sup>1</sup>, Aakash Aanegola<sup>1</sup>, 
Arun Kumar Singh<sup>2</sup>, K. Madhava Krishna<sup>1</sup></p>
<p align="center">  (1- Robotics Research Center, IIIT Hyderabad,  2- University of Tartu, Estonia)</p>


## Abstract


## Scenarios Simulated



[//]: # (Paste images in this section before the table)

## Sources of Uncertainity


<table>
  <tr>
    <td><img src="/README/imgs/uncertain1.png" alt="Image 1"></td>
    <td><img src="/README/imgs/uncertain2.png" alt="Image 2"></td>
  </tr>
</table>


## Dealing with Uncertainty - Parametric Assumption
![uncertain4](/README/imgs/uncertain4.png)
- Assumes shape of underlying distribution 
- Can lead to conservative behaviour
- Does not handle Noisy Annotations
- 
## We propose …. UAP-BEV
![bev](/README/imgs/bev.png)




## Part 1: Augmenting Uncertainty into Distance Estimates
![Estimate](/README/imgs/estimate.png)

## Part 2: Efficient Batch Optimization with Constrained Projection
![efficient](/README/imgs/efficient.png)




## Results

![result](/README/imgs/results.png)

## Longitudinal Barrier Ablation
![lba](/README/imgs/lba.png)

## CEM Analysis
![cem](/README/imgs/CEM.png)

**a.** **The histogram of constraint violation functions for each set in the elite set. At the start, multiple samples are spread out on non-zero values, complete convergence is achieved and at Iteration 10, all samples have values 0.**  
  
  
**b.** **Convergence of normalized costs with trace of covariance, signifying the samples are pushed towards good regions.**  







## Sources of Aleatoric Uncertainty
- Noise in RGB Images
- Noise in Intrinsics, error in GPS.
- Noisy BEV annotations

















