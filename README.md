![banner-logo](doc/imgs/banner-plenoptic.png)

---

Datasets R12-ABC
===============

### Download link

The datasets can be downloaded [here](https://drive.uca.fr/f/2cea45f26455407497f3/?dl=1).

### Experimental setup

For all experiments we used a _Raytrix R12_ color 3D-light-field-camera, with a _MLA_ of F/2.4 aperture.
The camera is in Galilean _internal_ configuration.
The mounted lens is a _Nikon AF Nikkor F/1.8D_ with a `50 mm` focal length.
The _MLA_ organization is hexagonal row-aligned, and composed of `176 x 152` (width x height) micro-lenses with `I = 3` different types.
The sensor is a _Basler beA4000-62KC_ with a pixel size of `s = 0.0055 mm`.
The raw image resolution is `4080 x 3068`.

### Datasets

We introduce three new datasets for three different focus distance configurations `h`, namely :

- **R12-A** for `h = 450 mm`,
- **R12-B** for `h = 1000 mm`, 
- and **R12-C** for `h = inf`.

**Note** that when changing the focus setting, the main lens moves with respect to the block MLA-sensor.

Each dataset is composed of:

- white raw plenoptic images acquired at different apertures (`N in {4, 5.66, 8, 11.31, 16}`) using a light diffuser mounted on the main objective for pre-calibration step,
- free-hand calibration targets acquired at various poses (in distance and orientation), separated into two subsets, one for the calibration process (16 images) and the other for reprojection error evaluation (15 images),
- a white raw plenoptic image acquired in the same luminosity condition and with the same aperture as in the calibration targets acquisition for devignetting,
- and calibration targets acquired with a controlled translation motion for quantitative evaluation, along with the depth maps computed by the [Raytrix](https://raytrix.de/) software (_RxLive  v4.0.50.2_).

We use a `9 x 5` of `10 mm` side checkerboard for R12-A, 
a `8 x 5` of `20 mm` for R12-B,
and a `6 x 4` of `30 mm` for R12-C.

### Software and setup

All images has been acquired using the free software _MultiCam Studio_ (v6.15.1.3573) of the company [Euresys](https://www.euresys.com/en/Homepage).
The shutter speed has been set to `5 ms`.
While taking white images for the pre-calibration step, the gain has been set to its maximum value.
For [Raytrix](https://raytrix.de/) data, we use their proprietary software _RxLive_ (v4.0.50.2) to calibrate the camera, and compute the depth maps used in the evaluation.


Dataset R12-D
===============

### Download link

The dataset can be downloaded [here](https://drive.uca.fr/f/5da7e8cc5d22467989e0/?dl=1).

### Experimental setup

For all experiments we used a _Raytrix R12_ color 3D-light-field-camera, with a _MLA_ of F/2.4 aperture.
The camera is in Galilean _internal_ configuration.
The mounted lens is a a _Nikon AF DC-Nikkor F/2D_ with a `135 mm` focal length.
The _MLA_ organization is hexagonal row-aligned, and composed of `176 x 152` (width x height) micro-lenses with `I = 3` different types.
The sensor is a _Basler beA4000-62KC_ with a pixel size of `s = 0.0055 mm`.
The raw image resolution is `4080 x 3068`.

### Dataset

The dataset is capture at focus distance configuration `h = 1500 mm`.

The dataset is composed of:

- white raw plenoptic images acquired at different apertures (`N in {4, 5.66, 8, 11.31, 16}`) using a light diffuser mounted on the main objective for pre-calibration step,
- free-hand calibration targets acquired at various poses (in distance and orientation), separated into two subsets, one for the calibration process (16 images) and the other for reprojection error evaluation (15 images),
- a white raw plenoptic image acquired in the same luminosity condition and with the same aperture as in the calibration targets acquisition for devignetting,
- and calibration targets acquired with a controlled translation motion for quantitative evaluation, along with the depth maps computed by the [Raytrix](https://raytrix.de/) software (_RxLive  v4.0.50.2_).

We use a `5 x 3` of `20 mm` side checkerboard.

### Software and setup

All images has been acquired using the free software _MultiCam Studio_ (v6.15.1.3573) of the company [Euresys](https://www.euresys.com/en/Homepage).
The shutter speed has been set to `5 ms`.
While taking white images for the pre-calibration step, the gain has been set to its maximum value.
For [Raytrix](https://raytrix.de/) data, we use their proprietary software _RxLive_ (v4.0.50.2) to calibrate the camera, and compute the depth maps used in the evaluation.

Dataset UPC-S
===============

Simulated dataset for Lytro-like plenoptic camera configuration, i.e., _unfocused_ plenoptic camera (UPC).

### Download link

The dataset can be downloaded [here](https://drive.uca.fr/f/d765fe50325140baab86/?dl=1).

### Experimental setup

We used the _Lytro Illum_ intrinsic parameters reported in Table 4 of Bok et al. (2017) as baseline for the simulation, corresponding to a main lens of aperture `F/2` with a `9.9845 mm` focal length.
The camera is in unfocused _internal_ configuration (i.e., `f = d`).
The MLA organization is hexagonal row-aligned, and composed of `541 x 434` (width x height) micro-lenses of the same type (`I = 1`).
The raw image resolution is `7728 x 5368` pixel, with a pixel size of `s = 0.0014 mm` and with micro-image of radius `7.172` pixel. 

### Dataset

The dataset is correspond to the focus distance configuration `h = hyperfocal`.

The dataset is composed of:

- white raw plenoptic images simulated at different apertures (`N in {2, 4, 5.6}`) for pre-calibration step,
- free-hand calibration targets simulated at various poses (in distance and orientation), separated into two subsets, one for the calibration process and the other for reprojection error evaluation,
- and calibration targets with known translation along the z-axis for quantitative evaluation.

We use a `9 x 5` of `26.25 mm` side checkerboard.

### Software and setup

All images has been generated using the [libpleno] and our raytracing simulator [PRISM].


Dataset R12-E, ES, ELP20
===============

Datasets containing ground truth data on 3D complex real-world scene acquired with a 3D lidar scanner Leica ScanStation P20 (LP20).

### Download link

The datasets can be downloaded [here](https://drive.uca.fr/f/f164345e148642b881c3/?dl=1).

### Experimental setup 

For our experiments we used a _Raytrix R12_ color 3D-light-field-camera, with a MLA of F/2.4 aperture.
The camera is in Galilean internal configuration.
The mounted lens is a _Nikon AF Nikkor F/1.8D_ with a `50 mm` focal length.
The MLA organization is hexagonal row-aligned, and composed of `176 x 152` (width x height) micro-lenses with `I = 3` different types.
The sensor is a _Basler beA4000-62KC_ with a pixel size of `s = 0.0055 mm`.
The raw image resolution is `4080 x 3068 pixel`.

All images have been acquired using the _MultiCamStudio_ free software (v6.15.1.3573) of the [Euresys](https://www.euresys.com/en/Homepage) company.
We set the shutter speed to `5 ms`.

**3D scenes setup.** We use a 3D lidar scanner, a _Leica ScanStation P20 (LP20)_, that allows us to capture a color point cloud with high precision that can be used as ground truth data. 
The _LP20_ is configured with no HDR and with a resolution of 1.6 mm @ 10 m.

### Datasets

The configuration corresponds to a focus distance `h = 2133 mm`.
We built a calibration dataset, using a `6 x 4` of `30 mm` side checkerboard, which is composed of:

- white raw plenoptic images acquired at different apertures (`N in {2.8, 4, 5.66, 8, 11.31, 16}`) using a light diffuser mounted on the main objective for pre-calibration,
- free-hand calibration target images acquired at various poses (in distance and orientation) for the calibration process (31 images),
- a white raw plenoptic image acquired in the same luminosity condition and with the same aperture as in the calibration targets acquisition for devignetting.

With this configuration, we created two sub-datasets:
- a simulated dataset built upon our own simulator [PRISM] based on raytracing to generate images (with `1500 rays/pixel`) with known absolute position for quantitative evaluation, named **R12-ES** (15 images, from `500 mm` to `1900 mm` with a step of `100 mm`);
- a dataset composed of several 3D scenes with ground truth acquired with the _LP20_, for object distances ranging from `400 mm` to `1500 mm`.

The latter dataset, named **R12-ELP20**, includes fives scenes: 

- one scene for extrinsic parameters calibration, containing checker corner targets, named _Calib_;
- two scenes containing textured planar objects, named _Plane-1_ and _Plane-2_;
- and two more complex scenes containing various figurines, named _Figurines-1_ and _Figurines-2_.

Each scene is composed of: a colored point cloud (with spatial (x,y,z) information, color information (r,g,b), and intensity information) in format `.ptx`, `.pts` and `.xyz`; 3D positions of the targets in the lidar reference frame; two raw plenoptic images in _rgb_ color and two raw plenoptic images in bayer; finally, photos and labels of the scene.


Applications
============

For instance, the datasets can be used with the following applications :
 * [COMPOTE] (Calibration Of Multi-focus PlenOpTic camEra), a collection of tools to pre-calibrate and calibrate (multifocus) plenoptic cameras.
 * [PRISM] (Plenoptic Raw Image Simulator), a collection of tools to generate and simulate raw images from (multifocus) plenoptic cameras.
 * [BLADE] (BLur Aware Depth Estimation with a plenoptic camera), a collection of tools to estimate depth map from raw images obtained by (multifocus) plenoptic cameras.

Based on the [libpleno], an open-source C++ computer-vision library for plenoptic cameras modeling and processing.


Citing
======

If you use our datasets, the [libpleno], the [COMPOTE] tools, the [PRISM] tools or the [BLADE] tools in an academic context, please cite the following publication:

	@inproceedings{labussiere2020blur,
	  title 	=	{Blur Aware Calibration of Multi-Focus Plenoptic Camera},
	  author	=	{Labussi{\`e}re, Mathieu and Teuli{\`e}re, C{\'e}line and Bernardin, Fr{\'e}d{\'e}ric and Ait-Aider, Omar},
	  booktitle	=	{Proceedings of the IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
	  pages		=	{2545--2554},
	  year		=	{2020}
	}
	
or 

	@article{labussiere2021calibration
	  title	    =	{Leveraging blur information for plenoptic camera calibration},
	  author	=	{Labussi{\`e}re, Mathieu and Teuli{\`e}re, C{\'e}line and Bernardin, Fr{\'e}d{\'e}ric and Ait-Aider, Omar},
	  journal	=	{arXiv preprint arXiv:2111.05226},
	  year		=	{2021}
	}

License
=======

This work is licensed under the [Creative Commons Attribution-NonCommercial 4.0 International License](https://creativecommons.org/licenses/by-nc/4.0/). Enjoy!

[Ubuntu]: http://www.ubuntu.com
[CMake]: http://www.cmake.org
[CMake documentation]: http://www.cmake.org/cmake/help/cmake2.6docs.html
[git]: http://git-scm.com
[Eigen]: http://eigen.tuxfamily.org
[libv]: http://gitlab.ip.uca.fr/libv/libv
[lma]: http://gitlab.ip.uca.fr/libv/lma
[OpenCV]: https://opencv.org/
[Doxygen]: http://www.stack.nl/~dimitri/doxygen/
[boost]: http://www.boost.org/
[libpleno]: https://github.com/comsee-research/libpleno
[COMPOTE]: https://github.com/comsee-research/compote
[BLADE]: https://github.com/comsee-research/blade
[PRISM]: https://github.com/comsee-research/prism


---
