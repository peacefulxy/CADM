# CADM
Complexity-Adaptive Distance Metric for Object Proposals Generation - CVPR2015

Yao Xiao <yxiaoab@cse.ust.hk>
June 2015
-------------------------------------------------------------------------------

1. Installation
All the dependency libraries are provided and compiled. For Linux and Windows 
the compiled mex files are provided as well. For Mac please compile all the cpp
files in ./mex folder. 

2. Getting Started
Demo.m load an image and output the bounding box proposals of potential objects.
The ground truth location and the closest proposals are displayed and overlap 
scores are marked. 
DemoVOC2012.m evaluate the algorithm on the PASCAL VOC2012 validation dataset. 
Please create a folder ./VOCdevkit under the root path and move the VOC2012 dataset 
into it. After evaluation the MABOs are calculated and recall-threshold score curve 
is drawn.

3. Parameters Setting
Default setting:
opts.merge.Wgraph = [1, 0.4];
opts.merge.Wmaxmin = [0, 6];
use 2*2 branches to increase diversity. Another setting:
opts.merge.Wgraph = [1, 0.7, 0.4];
opts.merge.Wmaxmin = [0, 3, 6, 9];
produce higher MABO and AUC, especially more accurate in high overlap section. While 
the running time increase accordingly. 
