# note for ORB-SLAM2
---
**reference**

*ORB-SLAM*
https://github.com/raulmur/ORB_SLAM2
https://github.com/stevenlovegrove/Pangolin
https://blog.csdn.net/FRIGIDWINTER/article/details/119900292
https://blog.csdn.net/qq_42037180/article/details/88371971

[install-opencv](https://blog.csdn.net/echoamor/article/details/83022352)

##install

**attention**
1. To intsall the Pangolin,you should pay attention to its version,maybe give up the git,choose the release tag is a better idea.Or you may meet the problem about the **"Eigen3::Eigen" but the target was not found."**
2. To install the opencv by build from the source code,the verion of [opencv_contrib](https://github.com/opencv/opencv_contrib/tags) and [opencv](https://github.com/opencv/opencv/tags)must be match with each other.
3. The opencv can be installed by cmake-gui .
4. To install the ORB-SLAM,At first, you should use the [./build.sh] to build [DBoW2],[g2o],[ORB-SLAM],etc .Then you should use [./build_ros.sh] to build [ORB-SLAM] in the ROS envs.
 
---

##Issues




