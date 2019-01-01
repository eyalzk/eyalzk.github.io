---
layout: post
title:  "Neural Style Transfer"
date:   2017-03-15 08:00:00
author: Eyal Zakkay
categories:
<!-- tags:	jekyll welcome -->
cover:  "/assets/sketch/cat_interp.svg"
git_url: "https://github.com/eyalzk/sketch_rnn_keras"
url_overide: "https://github.com/eyalzk/style_transfer"
img: "/assets/neural_style/eye.jpg"
---


Tensorflow implementation of the paper ["A Neural Algorithm of Artistic Style"](https://arxiv.org/abs/1508.06576).

The algorithm renders an image that keeps the content of one reference image while copying the style of another.




<img src="images/result/eagle3/eagle&psy21.jpg" width="790">







## Dependencies:
* [Tensorflow](https://www.tensorflow.org/install/) (version > 1.0)
* [tensorflow-vgg](https://github.com/machrisaa/tensorflow-vgg)

## Usage:
Most parameters can be configured when running using command line, though some parameters can currently be configured only through default_params.py.

To run using command line:

`python main.py`

All parameters are optional and have default values:

`--iterations <number of iterations>`, `--out_width <width of output image>`, `--content_path <content file path>`, `--style_path <style file path>`, `--result_path <Path of output image (with extension). If only a directory path is given, an automatic file name will be generated>`, `--noise_ratio <init image is noise_ratio*noise + (1-noise_ratio)*content_image>`, `--gamma <content/style ratio>`, `--beta <style weight>`, `--theta <tv loss weight>`, `--optimizer <'adam' or 'lbfgs'>`.

## Acknowledgements
For the trained VGG19 I have used the implementation of [mechrisaa](https://github.com/machrisaa/tensorflow-vgg).


### Photo credits:

1. [Eagle](https://www.flickr.com/photos/jacobmeredith/)
2. [Psychedelic art](http://wallpaperspack.info/?p=52239)
