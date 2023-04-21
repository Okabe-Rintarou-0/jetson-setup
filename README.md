# 环境搭建

## 系统信息

设备：JETSON XAVIER NX

系统：aarch64 ubuntu 18.04

语言：python 3.6

## 搭建过程

配置 ssd：https://blog.csdn.net/weixin_47606814/article/details/127841948

安装 aarch64 系统对于的 anaconda：https://blog.csdn.net/yuehenmiss/article/details/125412725（本身是个替代品，见 https://blog.csdn.net/qq_37700257/article/details/123640826）

opencv：https://sjtu-robomaster-team.github.io/campus-competition-1-opencv-environment/

cuda、cudnn：https://www.jianshu.com/p/33cd8368b2ca

pytorch：

- https://forums.developer.nvidia.com/t/pytorch-for-jetson/72048 
- https://blog.csdn.net/qq_41426807/article/details/124705416

librealsense2：https://github.com/IntelRealSense/librealsense/blob/master/doc/distribution_linux.md

pyrealsense2(没有 arm 版本的库，必须 build from source)：

- https://www.lieuzhenghong.com/how_to_install_librealsense_on_the_jetson_nx/
- https://github.com/IntelRealSense/librealsense/issues/6964#issuecomment-707501049
- https://github.com/IntelRealSense/librealsense/issues/1657#issuecomment-386550240
- https://blog.csdn.net/qq_37509948/article/details/118195939

    具体步骤：

    - 按照上面第一个链接提供的方式下载，不过如果系统存在其他版本 python（非3.6），则需要按照第二个链接里的步骤进行

    - 如果用的是 anaconda，需要按照第三个链接的方式添加一个 soft-link 到 conda 对应环境的 site-packages 里面。