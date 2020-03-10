![banner-logo](doc/imgs/banner-plenoptic.png)

---

Datasets R12-ABC
===============

### Download link

The datasets can be downloaded [here](https://drive.uca.fr/f/d3a73cb1926047a8b635/?dl=1).

### Experimental setup

For all experiments we used a _Raytrix R12_ color 3D-light-field-camera, with a _MLA_ of F/2.4 aperture.
The mounted lens is a _Nikon AF Nikkor F/1.8D_ with a `50 mm` focal length.
The _MLA_ organization is hexagonal, and composed of `176 x 152` (width x height) micro-lenses with `I = 3` different types.
The sensor is a _Basler beA4000-62KC_ with a pixel size of `s = 0.0055 mm`.
The raw image resolution is `4080 x 3068`.

### Datasets

We introduce three new datasets for three different focus distance configurations `h`, namely :

- **R12-A** for `h = 450 mm`,
- **R12-B** for `h = 1000 mm`, 
- and **R12-C** for `h = inf`.

Each dataset is composed of:

- white raw plenoptic images acquired at different apertures (`N in {4, 5.66, 8, 11.31, 16}`) with augmented gain to ease circle detection in the pre-calibration step,
- free-hand calibration targets acquired at various poses (in distance and orientation), separated into two subsets, one for the calibration process and the other for the qualitative evaluation,
- a white raw plenoptic image acquired in the same luminosity condition and with the same aperture as in the calibration targets acquisition,
- and calibration targets acquired with a controlled translation motion for quantitative evaluation, along with the depth maps computed by the [Raytrix](https://raytrix.de/) software (_RxLive  v4.0.50.2_).


We use a `9 x 5` of `10 mm` side checkerboard for R12-A, 
a `8 x 5` of `20 mm` for R12-B,
and a `7 x 5` of `30 mm` for R12-C.

### Software and setup

All images has been acquired using the free software _MultiCam Studio_ (v6.15.1.3573) of the company [Euresys](https://www.euresys.com/en/Homepage).
The shutter speed has been set to `5 ms`.
While taking white images for the pre-calibration step, the gain has been set to its maximum value.
For [Raytrix](https://raytrix.de/) data, we use their proprietary software _RxLive_ (v4.0.50.2) to calibrate the camera, and compute the depth maps used in the evaluation.


Applications
============

For instance, the datasets can be used with the following applications :
 * [COMPOTE] (Calibration Of Multi-focus PlenOpTic camEra), a collection of tools to pre-calibrate and calibrate a multifocus plenoptic camera.
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
[libpleno]: http://gitlab.ip.uca.fr/mla-dev/libpleno
[COMPOTE]: http://gitlab.ip.uca.fr/mla-dev/compote


---
