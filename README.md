1.首先按照本文内容选数据集进行预处理（RESIDE数据集链接https://sites.google.com/view/reside-dehaze-datasets，

O-Haze数据集链接https://data.vision.ee.ethz.ch/cvl/ntire18//o-haze/）。

2.运用CycleGAN网络学习真实雾特征。其中预处理后的真实雾图放在\cyclegan+pix2pix\datasets\facades\trainB文件夹中,原始干净图片放在\cyclegan+pix2pix\datasets\facades\trainA文件中。

训练好的模型用来给原始干净图片赋予真实雾特征并与自身构成匹配数据集。

3.将制作好的匹配数据集放入Pix2pix网络训练去雾模型。

4.用于验证数据合成方法可行性的去雾网络，只需要将制作好的匹配数据集放入相应的路径进行训练测试即可。

验证数据合成方法可行性的去雾网络的详细介绍见下方：

AOD-Net:"AOD-Net: All-in-One Dehazing Network"（https://openaccess.thecvf.com/content_ICCV_2017/papers/Li_AOD-Net_All-In-One_Dehazing_ICCV_2017_paper.pdf）

PCFAN:"Pyramid Channel-based Feature Attention Network for image dehazing"（https://doi.org/10.1016/j.cviu.2020.103003）

GridDehazeNet:"GridDehazeNet: Attention-Based Multi-Scale Network for Image Dehazing"（https://arxiv.org/abs/1908.03245v1）

5.最后提升分辨率的算法选用的是Real-ESRGAN,来源于https://github.com/xinntao/Real-ESRGAN，相应的参考文献题目为*Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data*（https://arxiv.org/abs/2107.10833）。

如遇到任何问题欢迎联系handandong@163.com；SuXinyu_twoslucky@163.com。



1.Firstly, preprocess the selected datasets according to the content of this paper. The RESIDE dataset can be accessed at https://sites.google.com/view/reside-dehaze-datasets, and the O-Haze dataset can be accessed at https://data.vision.ee.ethz.ch/cvl/ntire18//o-haze/.

2.Utilize the CycleGAN network to learn real haze characteristics. Place the preprocessed real haze images in the "\cyclegan+pix2pix\datasets\facades\trainB" folder, and place the original clean images in the "\cyclegan+pix2pix\datasets\facades\trainA" folder. 

The trained model will be used to impart real haze characteristics to the original clean images, creating a paired dataset.

3.Train the dehazing model using the Pix2pix network with the created paired dataset.

4.To test the feasibility of the data synthesis method for dehazing networks, you only need to place the created paired dataset in the appropriate path for training and testing.

The detailed introduction to the dehazing network for verifying the feasibility of data synthesis methods can be found below：

AOD-Net: "AOD-Net: All-in-One Dehazing Network" (https://openaccess.thecvf.com/content_ICCV_2017/papers/Li_AOD-Net_All-In-One_Dehazing_ICCV_2017_paper.pdf)

PCFAN: "Pyramid Channel-based Feature Attention Network for image dehazing" (https://doi.org/10.1016/j.cviu.2020.103003)

GridDehazeNet: "GridDehazeNet: Attention-Based Multi-Scale Network for Image Dehazing" (https://arxiv.org/abs/1908.03245v1)

5.Finally, employ the Real-ESRGAN algorithm for resolution enhancement, which can be found at https://github.com/xinntao/Real-ESRGAN. The corresponding reference paper is titled "Real-ESRGAN: Training Real-World Blind Super-Resolution with Pure Synthetic Data."（https://arxiv.org/abs/2107.10833）.

If you have any questions, please feel free to contact handandong@163.com or SuXinyu_twoslucky@163.com.