![banner-logo](doc/imgs/banner-plenoptic.png)

---

Datasets R12-ABC
===============

### Download link

The datasets can be downloaded [here](https://drive.uca.fr/f/d3a73cb1926047a8b635/?dl=1).

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

The dataset can be downloaded [here](https://drive.uca.fr/f/bde8b32c892243ff95c4/?dl=1).

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

The dataset can be downloaded [here](https://drive.uca.fr/f/c617039b1dd14ad78e84/?dl=1).

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


Applications
============

For instance, the datasets can be used with the following applications :
 * [COMPOTE] (Calibration Of Multi-focus PlenOpTic camEra), a collection of tools to pre-calibrate and calibrate a multifocus plenoptic camera.
 * [PRISM] (Plenoptic Raw Image Simulator), a collection of tools to generate and simulate raw images from a multifocus plenoptic camera.
 * [BLADE] (BLur Aware Depth Estimation with a multifocus plenoptic camera), a collection of tools to estimate depth map and generate point clouds from raw images obtained by a multifocus plenoptic camera.
 * [libpleno], an open-souce C++ library for plenoptic camera.


Citing
======

If you use our datasets, the [libpleno] or the [COMPOTE] tools in an academic context, please cite the following publication:

	@inproceedings{Labussiere2020,
		author = {Labussi{\`{e}}re, Mathieu and Teuli{\`{e}}re, C{\'{e}}line and Bernardin, Fr{\'{e}}d{\'{e}}ric and Ait-Aider, Omar},
		booktitle = {2020 IEEE/CVF Conference on Computer Vision and Pattern Recognition (CVPR)},
		title = {{Blur Aware Calibration of Multi-Focus Plenoptic Camera}},
		year = {2020}
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
