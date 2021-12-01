# Note for gpd(6 DOF Grasp Pose Detection )

[gpd](https://github.com/atenpas/gpd)
[gpd_ros](https://github.com/atenpas/gpd_ros)

[pcl_official](https://pcl.readthedocs.io/projects/tutorials/en/latest/compiling_pcl_posix.html)
[pcl_install_CSDN_1](https://blog.csdn.net/czychen1997/article/details/107306674/)
[pcl_install_CSDN_2](https://blog.csdn.net/qq_36728314/article/details/89487719)
[pcl_install_CSDN_3](https://www.cnblogs.com/winslam/p/12074432.html)
[opencv-install-CSDN](https://blog.csdn.net/echoamor/article/details/83022352)

## Install

**Attention**

1. the version between the vtk and pcl must be matched like below:
(however the gpd project need the version of pcl >= 1.9.0 )

pcl-1.7.2          vtk-5.10.1 / vtk-6.2.0
pcl-1.8.1          vtk-7.1.1
pcl-1.9.1          vtk-8.2.0(or8.1)

You can dowload the suitable version vtk in [VTK](https://vtk.org/download/)
2. Download the [metslib](https://www.coin-or.org/download/source/metslib/metslib-0.5.3.tgz)  and install by:

'''
tar xzvf metslib-0.5.3.tgz
cd metslib-0.5.3
./configure
make -j
sudo make install
'''

This package is needed in compiling the pcl 
3.   When you try to generate the makefile by 
'
cmake -DCMAKE_BUILD_TYPE=None -DCMAKE_INSTALL_PREFIX=/usr \ -DBUILD_GPU=ON-DBUILD_apps=ON -DBUILD_examples=ON \ -DCMAKE_INSTALL_PREFIX=/usr ..

'
you must check the output in terminate carefully, especial the messages about **"not found"**.
However ,there are always some "not found" can not solve,just forget it

4. When you try to **make** it, some errors may be happend ,

**Error_1** pcl_visualizer.cpp:3567:88.
follow the [pcl_install_CSDN_1](https://blog.csdn.net/czychen1997/article/details/107306674/)

**Error_2** like [this](https://github.com/atenpas/gpd/issues/107)
Just follow this [push](https://github.com/atenpas/gpd/pull/109),modify the CmakeList.txt 

Look for the solutions in github is a good idea.

And one more thing,don't forget instal by

'
sudo make install
'

5. When you change the VTK's verison in your ubuntu ,you may break your ROS environments,some ros packages should be reinstalled again,don't worry ,it is a small question.

6. When you try to test the GPD by
'''
./detect_grasps ../cfg/eigen_params.cfg ../tutorials/krylon.pcd

'''

 You may meet the error : **Failed to find match for field 'rgb'**
Just follow [this](https://blog.csdn.net/weixin_37835423/article/details/105363615) check the pcd file and modify the **TYPE** in the krylon.pcd to
'
TYPE F F F U
'





