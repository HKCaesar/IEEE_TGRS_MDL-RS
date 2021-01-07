# More Diverse Means Better: Multimodal Deep Learning Meets Remote-Sensing Imagery Classification

[Danfeng Hong](https://sites.google.com/view/danfeng-hong), [Lianru Gao](https://scholar.google.com/citations?hl=en&user=f6OnhtcAAAAJ), [Naoto Yokoya](https://naotoyokoya.com/), [Jing Yao](https://scholar.google.com/citations?user=1SHd5ygAAAAJ&hl=en), [Jocelyn Chanussot](http://jocelyn-chanussot.net/), [Qian Du](https://scholar.google.com/citations?user=0OdKQoQAAAAJ&hl=en), [Bing Zhang](http://english.radi.cas.cn/Education/PhDS/201401/t20140109_115415.html)

___________

The code in this toolbox implements the ["More Diverse Means Better: Multimodal Deep Learning Meets Remote-Sensing Imagery Classification"](https://ieeexplore.ieee.org/document/9174822). More specifically, it is detailed as follow.

![alt text](./Motivation.png)


Citation
---------------------

**Please kindly cite the papers if this code is useful and helpful for your research.**

Danfeng Hong, Lianru Gao, Naoto Yokoya, Jing Yao, Jocelyn Chanussot, Qian Du, Bing Zhang. More Diverse Means Better: Multimodal Deep Learning Meets Remote-Sensing Imagery Classification, IEEE Transactions on Geoscience and Remote Sensing, 2020, DOI: 10.1109/TGRS.2020.3016820. 

     @article{hong2020more,
      title     = {More Diverse Means Better: Multimodal Deep Learning Meets Remote-Sensing Imagery Classification},
      author    = {D. Hong and L. Gao and N. Yokoya and J. Yao and J. Chanussot and Q. Du and B. Zhang},
      journal   = {IEEE Trans. Geosci. Remote Sens.}, 
      year      = {2020},
      note      = {DOI:10.1109/TGRS.2020.3016820},
      publisher = {IEEE}
     }

System-specific notes
---------------------
The data were generated by Matlab R2016a or higher versions, and the codes of various networks were tested in Tensorflow in Python 3.7 on Windows 10 machines.

How to use it?
---------------------
This toolbox consists of two different network architectures, i.e., fully-connected networks (FC-Nets), convolutional neural networks (CNNs). Each of network architectures also includes different fusion networks. For more details, please refer to the paper.

Here an example experiment is given by using **Houston2013 hyperspectral and LiDAR data**. Directly run .py functions with different networks to produce the results. Please note that due to the randomness of the parameter initialization, the experimental results might have slightly different from those reported in the paper.

One trick to clarify the differences between cross-modality learning (CML) and multi-modality learning (MML) is the use of batch normalization (BN). In the test phase, the BN should be open in CML, while the BN should be close in MML. Because in CML, one modality is missing, i.e., it is set to be 0, in this case, the BN is close (i.e., using the mean vaule obtained from the training samples), it would generate the bad inference.

:exclamation: You may need to manually download `HSI_TeSet.mat` and `HSI_TrSet.mat` to your local in the folder under path `IEEE_TGRS_MDL-RS/MDL-RS_CNNs/HSI_LiDAR_CNN/`, due to their too large file size, from the following links of google drive or baiduyun:

Google drive: https://drive.google.com/file/d/1vno8vQxCXgr7xk-Nez9CVbJmjkDMBCbe/view?usp=sharing

Baiduyun: https://pan.baidu.com/s/1ug_tKyrbwg_CzHGpB2YK2A (access code: hfw3)


**If you are interested in LCZ classification datasets, please download them from here: [Baiduyun](https://pan.baidu.com/s/1dYkaUm4JTjOWdtx79RsB6w) with access code (gkli)!**

If you want to run the code in your own data, you can accordingly change the input (e.g., data, labels) and tune the parameters.

If you encounter the bugs while using this code, please do not hesitate to contact us.

Licensing
---------

Copyright (C) 2020 Danfeng Hong

This program is free software: you can redistribute it and/or modify it under the terms of the GNU General Public License as published by the Free Software Foundation, version 3 of the License.

This program is distributed in the hope that it will be useful, but WITHOUT ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU General Public License for more details.

You should have received a copy of the GNU General Public License along with this program.

Contact Information:
--------------------

Danfeng Hong: hongdanfeng1989@gmail.com<br>
Danfeng Hong is with the Univ. Grenoble Alpes, CNRS, Grenoble INP, GIPSA-lab, 38000 Grenoble, France.

If emergency, you can also add my QQ: 345088114.
