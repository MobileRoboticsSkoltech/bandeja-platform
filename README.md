# SmartDepthSync: Open Source Synchronized Video Recording System of Smartphone RGB and Depth Camera Range Image Frames with Sub-millisecond Precision

<p align="center">
  <img src="common.png"/>
</p>

This is a repository that gathers open-source materials introduced and described in the SmartDepthSync paper ([IEEE link](https://ieeexplore.ieee.org/document/9709778/),
[arXiv link](https://arxiv.org/abs/2111.03552)). In addition to the paper, some description can be found in the links in the table below. The table keeps all the important link to the building parts of the system depicted in the image.  

The materials represent diverse software and their own functionality launched on different hardware:
<table>
    <tr> <td>Material</td> <td>Function</td> <td>Launched on</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bandeja-wrapper/tree/19deb471355687901d7c3812a64ab3299d4db7a5">Python launcher</a> </td> <td>command-line tool that is entry point for setup (launch of sensors, synchronization) and recording to ROS bag file procedures</td> <td> mini-PC </td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bandeja-ros-src/tree/164b2ff17e6f09a3bc60ea67868f0ec08da14652">ROS source code</a> </td> <td>driver for setting up and gathering data from the sensors (Azure Kinect DK depth camera and MCU board with IMU sensor)</td> <td>mini-PC</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bandeja-mcu-firmware/tree/8867c939f899722ea3f51e7653b303456a2425bd">MCU firmware</a> </td> <td>responsible for synchronized depth camera triggering and IMU data gathering</td> <td>MCU board</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/OpenCamera-Sensors">OpenCamera-Sensors</a> </td> <td>smartphone application that records RGB video data and provides timestamps for synchronized depth camera triggering.  </td> <td>smartphone</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bag-extractor">bag-extractor</a> </td> <td>CLI-script that extracts recorded ROS bag files to images and other data types distributed to paths</td> <td>any PC</td> </tr>
</table>

For entire clone with submodules:
```
git clone --recurse-submodules https://github.com/MobileRoboticsSkoltech/bandeja-platform
```

## Twist-n-Sync Python Package
Synchronization is based on our [Twist-n-Sync](https://github.com/MobileRoboticsSkoltech/twistnsync-python) algorithm that can be installed via `pip`.

Using this materials please do not forget to reference this repository and cite the paper:

```
@article{faizullin2022smartdepthsync,
  author={Faizullin, Marsel and Kornilova, Anastasiia and Akhmetyanov, Azat and Pakulev, Konstantin and Sadkov, Andrey and Ferrer, Gonzalo},
  title={SmartDepthSync: Open Source Synchronized Video Recording System of Smartphone RGB and Depth Camera Range Image Frames with Sub-millisecond Precision}, 
  journal={IEEE Sensors Journal}, 
  publisher={IEEE},
  year={2022},
  volume={22},
  number={7},
  pages={7043-7052},
  doi={10.1109/JSEN.2022.3150973}
}
```
