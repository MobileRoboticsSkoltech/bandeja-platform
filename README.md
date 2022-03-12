# SmartDepthSync: Open Source Synchronized Video Recording System of Smartphone RGB and Depth Camera Range Image Frames with Sub-millisecond Precision

This is a repository that gathers open-source materials introduced in the SmartDepthSync paper ([IEEE link](https://ieeexplore.ieee.org/document/9709778/),
[arXiv link](https://arxiv.org/abs/2111.03552)).

The materials represent diverse software their own functionality launched on different hardware:
<table>
    <tr> <td>Material</td> <td>Function</td> <td>Launched on</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bandeja-wrapper/tree/19deb471355687901d7c3812a64ab3299d4db7a5">Python launcher</a> </td> <td>command-line tool that is entry point for setup (launch of sensors, synchronization) and recording to ROS bag file procedures</td> <td> mini-PC </td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bandeja-ros-src/tree/164b2ff17e6f09a3bc60ea67868f0ec08da14652">ROS source code</a> </td> <td>driver for setting up and gathering data from the sensors (Azure Kinect DK depth camera and MCU board with IMU sensor)</td> <td>mini-PC</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bandeja-mcu-firmware/tree/8867c939f899722ea3f51e7653b303456a2425bd">MCU firmware</a> </td> <td>responsible for synchronized depth camera triggering and IMU data gathering</td> <td>MCU board</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/OpenCamera-Sensors">OpenCamera-Sensors</a> </td> <td>smartphone application that records RGB video data and provides timestamps for synchronized depth camera triggering.  </td> <td>smartphone</td> </tr>
    <tr> <td> <a href="https://github.com/MobileRoboticsSkoltech/bag-extractor">bag-extractor</a> </td> <td>CLI-script that extracts recorded ROS bag files to images and other data types distributed to paths</td> <td>any PC</td> </tr>
</table>

```
@article{faizullin2022smartdepthsync,
  author={Faizullin, Marsel and Kornilova, Anastasiia and Akhmetyanov, Azat and Pakulev, Konstantin and Sadkov, Andrey and Ferrer, Gonzalo},
  title={SmartDepthSync: Open Source Synchronized Video Recording System of Smartphone RGB and Depth Camera Range Image Frames with Sub-millisecond Precision}, 
  journal={IEEE Sensors Journal}, 
  publisher={IEEE},
  year={2022},
  volume={},
  number={},
  pages={1-1},
  doi={10.1109/JSEN.2022.3150973}
}
```
