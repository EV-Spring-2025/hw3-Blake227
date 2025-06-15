[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/SdXSjEmH)
# EV-HW3: PhysGaussian

This homework is based on the recent CVPR 2024 paper [PhysGaussian](https://github.com/XPandora/PhysGaussian/tree/main), which introduces a novel framework that integrates physical constraints into 3D Gaussian representations for modeling generative dynamics.

You are **not required** to implement training from scratch. Instead, your task is to set up the environment as specified in the official repository and run the simulation scripts to observe and analyze the results.


## Getting the Code from the Official PhysGaussian GitHub Repository
Download the official codebase using the following command:
```
git clone https://github.com/XPandora/PhysGaussian.git
```


## Environment Setup
Navigate to the "PhysGaussian" directory and follow the instructions under the "Python Environment" section in the official README to set up the environment.


## Running the Simulation
Follow the "Quick Start" section and execute the simulation scripts as instructed. Make sure to verify your outputs and understand the role of physics constraints in the generated dynamics.


## Homework Instructions
Please complete Part 1–2 as described in the [Google Slides](https://docs.google.com/presentation/d/13JcQC12pI8Wb9ZuaVV400HVZr9eUeZvf7gB7Le8FRV4/edit?usp=sharing).

## Simulation Videos
I simulated ficus (which material is jelly) and wolf (which material is sand). These are the baseline simulation videos.
[ficus_baseline](https://youtube.com/shorts/ZtiO-7FijjU)
[wolf_baseline](https://youtube.com/shorts/X-KFijX-MaY)
## Parametes adjusting
### Ficus

| `n_grid`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 30            |   38.26   |  ![gif](images/ficus_n_grid_30.gif)    |
| 35            |   38.16   |  ![gif](images/ficus_n_grid_35.gif)    | 
| 40  |   38.69   |  ![gif](images/ficus_n_grid_40.gif)    | 
| 45            |   38.47   |  ![gif](images/ficus_n_grid_45.gif)    | 
| 50   (baseline)         |   76.36   |  ![gif](images/ficus_n_grid_50.gif)    | 

| `substep_dt`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 2e-05         |   38.05   |  ![gif](images/ficus_substep_dt_2e-05.gif)    |
| 4e-05         |   38.13   |  ![gif](images/ficus_substep_dt_4e-05.gif)    | 
| 6e-05         |   38.34   |  ![gif](images/ficus_substep_dt_6e-05.gif)    | 
| 8e-05         |   38.96   |  ![gif](images/ficus_substep_dt_8e-05.gif)    | 
| 1e-04 (baseline)        |   76.54   |  ![gif](images/ficus_substep_dt_1e-04.gif)    | 

| `grid_v_damping_scale`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 0.0999            |   38.14   |  ![gif](images/ficus_grid_v_damping_scale_0.0999.gif)    |
| 0.4999            |   38.14   |  ![gif](images/ficus_grid_v_damping_scale_0.4999.gif)    | 
| 0.9999 (baseline) |   76.44   |  ![gif](images/ficus_grid_v_damping_scale_0.9999.gif)    | 
| 1.4999            |   37.65   |  ![gif](images/ficus_grid_v_damping_scale_1.4999.gif)    | 
| 1.9999            |   37.65   |  ![gif](images/ficus_grid_v_damping_scale_1.9999.gif)    | 

| `softening`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 0.001         |   76.40   |  ![gif](images/ficus_softening_0.001.gif)    |
| 0.005         |   76.11   |  ![gif](images/ficus_softening_0.005.gif)    | 
| 0.01          |   76.13   |  ![gif](images/ficus_softening_0.01.gif)    | 
| 0.05          |   76.15   |  ![gif](images/ficus_softening_0.05.gif)    | 
| 0.1           |   76.36   |  ![gif](images/ficus_softening_0.1.gif)    | 

### Wolf
| `n_grid`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 120            |   41.20   |  ![gif](images/wolf_n_grid_120.gif)    |
| 140            |   41.38   |  ![gif](images/wolf_n_grid_140.gif)    | 
| 160            |   41.72   |  ![gif](images/wolf_n_grid_160.gif)    | 
| 180            |   41.21   |  ![gif](images/wolf_n_grid_180.gif)    | 
| 200 (baseline) |   69.09   |  ![gif](images/wolf_n_grid_200.gif)    | 

| `substep_dt`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 1e-05         |    42.05   |  ![gif](images/wolf_substep_dt_1e-05.gif)    |
| 2e-05 (baseline)         |    69.09  |  ![gif](images/wolf_substep_dt_2e-05.gif)    | 
| 4e-05         |    42.08   |  ![gif](images/wolf_substep_dt_4e-05.gif)    | 
| 5e-05         |    41.65   |  ![gif](images/wolf_substep_dt_5e-05.gif)    | 
| 6e-04         |    39.55   |  ![gif](images/wolf_substep_dt_6e-05.gif)    | 

| `grid_v_damping_scale`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 0.0999            |   40.13   |  ![gif](images/wolf_grid_v_damping_scale_0.0999.gif)    |
| 0.4999            |   40.16   |  ![gif](images/wolf_grid_v_damping_scale_0.4999.gif)    | 
| 0.9999            |   42.49   |  ![gif](images/wolf_grid_v_damping_scale_0.9999.gif)    | 
| 1.4999            |   69.48   |  ![gif](images/wolf_grid_v_damping_scale_1.4999.gif)    | 
| 1.9999            |   68.96   |  ![gif](images/wolf_grid_v_damping_scale_1.9999.gif)    | 

| `softening`      |   PSNR    | GIF       | 
| ------------- | --------- | --------- |
| 0.001         |   69.43   |  ![gif](images/wolf_softening_0.001.gif)    |
| 0.005         |   69.30   |  ![gif](images/wolf_softening_0.005.gif)    | 
| 0.01          |   69.16   |  ![gif](images/wolf_softening_0.01.gif)    | 
| 0.05          |   69.33   |  ![gif](images/wolf_softening_0.05.gif)    | 
| 0.1           |   69.33   |  ![gif](images/wolf_softening_0.1.gif)    | 





## Disucssion
### n_grid
Determines the resolution of the background grid in the MPM solver.
In ficus simulation, as `n_grid` increases from 30 to 50 (baseline), the PSNR values rise from 38.26 → 38.16 → 38.69 → 38.47 → 76.36 at `n_grid=50`. The improvements below 50 are minor and far from the baseline. However, it is visually stable at low grid resolutions, the reason PSNR is low may be their outputs differ from `n_grid=50`
It shows PSNR heavily depends on spatial resolution, which means PSNR may not be a good metric to evaluate simulation quality when comparing between `n_grid`.

### substep_dt
Controls the size of the time step in each MPM update per frame.
In the wolf simulation, both increasing and decreasing substep_dt from the baseline lead to lower PSNR. Larger substep_dt causes overly aggressive motion per frame, while smaller values result in under-resolved dynamics. This highlights that substep_dt must be carefully balanced to preserve physical accuracy and visual consistency.
 
### grid_v_damping_scale
Controls the damping of velocity on the MPM grid after each step.
Testing values like 0.0999, 0.4999, 0.9999, 1.4999, and 1.9999, the highest PSNR occurs near the baseline (0.9999 = 76.44). Higher or lower values drop significantly (e.g., 1.9999 = 37.65). The damping factor must be carefully balanced. Around 1.0 yields optimal energy decay while preserving realism. Both under- and over-damping result in physical inconsistencies.


### softening
Modulates how the material reduces its internal stress after deformation, emulating plastic or soft materials.
Values ranging from 0.001 to 0.1 all yield similar PSNR scores (~76), nearly indistinguishable from the baseline.
For elastic materials like jelly, softening has little effect on physical behavior. Its influence would likely be more pronounced on plastic or metallic materials with permanent deformation.


# Reference
```bibtex
@inproceedings{xie2024physgaussian,
    title     = {Physgaussian: Physics-integrated 3d gaussians for generative dynamics},
    author    = {Xie, Tianyi and Zong, Zeshun and Qiu, Yuxing and Li, Xuan and Feng, Yutao and Yang, Yin and Jiang, Chenfanfu},
    booktitle = {Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition},
    year      = {2024}
}
```
