---
layout: post
title: "Data Fusion"
description: "导航定位中的数据融合算法"
categories: [Data]
tags: [code,Data]
redirect_from:
  - /2018/08/07/
---

>  导航定位中的数据融合算法


* Kramdown table of contents
{:toc .toc}

# IMU与里程计融合

Created 2018.08.07 by Sunnie; Last modified: 2018.08.07-V1.0

Contact :[1249053233@qq.com](mailto:1249053233@qq.com)

Copyleft! 2018 Yuqing Cao. Some rights reserved.

------

## 扩展卡尔曼滤波（Extended Kalman Filter）

#### 理论介绍

[卡尔曼滤波简介](https://blog.csdn.net/young_gy/article/details/78177291)

[卡尔曼滤波（一）csdn](https://blog.csdn.net/u012936940/article/details/76805526)

[卡尔曼滤波原理二：扩展卡尔曼](https://blog.csdn.net/u012936940/article/details/77249245)

[初学者的卡尔曼滤波](http://www.360doc.com/content/17/0113/15/19235756_622220370.shtml)

[扩展卡尔曼滤波EKF与多传感器融合](https://blog.csdn.net/young_gy/article/details/78468153)

[卡尔曼滤波的理解以及参数调整](https://blog.csdn.net/u013453604/article/details/50301477)

[卡尔曼滤波器学习笔记（一）](https://blog.csdn.net/lizilpl/article/details/45268471)

#### 代码示例

[KF&EKF及matlab代码地址](https://www.cnblogs.com/TIANHUAHUA/p/8473029.html)

[扩展卡尔曼滤波EKF及其MATLAB实现](http://blog.sina.com.cn/s/blog_ea828d2a0102wgun.html)

[C++下扩展卡尔曼类（EKF）的实现](https://blog.csdn.net/qiguizhe/article/details/78979715)

#### 结合ROS

[ROS与navigation教程-robot_pose_ekf](https://www.ncnynl.com/archives/201708/1909.html)

[03-数据融合-ROS轮式机器人数据融合-odom&IMU](https://www.jianshu.com/p/d19c249052e5)

[[ROS] 多传感器卡尔曼融合框架 Ethzasl MSF Framework 编译与使用](http://www.liuxiao.org/2016/07/ros-%e5%a4%9a%e4%bc%a0%e6%84%9f%e5%99%a8%e5%8d%a1%e5%b0%94%e6%9b%bc%e8%9e%8d%e5%90%88%e6%a1%86%e6%9e%b6-ethzasl-msf-framework-%e7%bc%96%e8%af%91%e4%b8%8e%e4%bd%bf%e7%94%a8/)

[使用robot_pose_ekf对传感器信息融合](http://www.dongcoder.com/detail-799955.html)

#### 论文实例

[陀螺仪+加速度+卡尔曼数据融合](https://wenku.baidu.com/view/ed337b8c856a561252d36f7f.html)

[基于惯性传感器和视觉里程计的机器人定位](https://wenku.baidu.com/view/c1ded71f7fd5360cba1adbeb.html)



# IMU内部数据融合

## ROS filter

[imu_complementary_filter](https://github.com/ccny-ros-pkg/imu_tools/tree/indigo/imu_complementary_filter)

## 互补滤波

[算法原理推导](https://blog.csdn.net/superrunner_wujin/article/details/77746582)

[浅谈陀螺仪和加速度计的互补滤波](https://blog.csdn.net/zhaojun1204/article/details/52790697)

[姿态解算进阶：互补滤波（陀螺仪、加速度计、地磁计数据融合）](https://blog.csdn.net/MOU_IT/article/details/80391216)

## 卡尔曼滤波

[MPU6050 + 一阶互补滤波+二阶互补滤波+卡尔曼滤波  +波形比较](https://blog.csdn.net/m0_37575064/article/details/76098588)

[互补滤波和卡尔曼滤波的融合姿态解算方法](http://www.doc88.com/p-2572805655284.html)



# 多传感器融合

[基于多传感器融合的室内机器人自主导航方法研究](http://f.wanfangdata.com.cn/www/%E5%9F%BA%E4%BA%8E%E5%A4%9A%E4%BC%A0%E6%84%9F%E5%99%A8%E8%9E%8D%E5%90%88%E7%9A%84%E5%AE%A4%E5%86%85%E6%9C%BA%E5%99%A8%E4%BA%BA%E8%87%AA%E4%B8%BB%E5%AF%BC%E8%88%AA%E6%96%B9%E6%B3%95%E7%A0%94%E7%A9%B6.ashx?isread=true&type=degree&resourceId=Y3226485&transaction=%7B%22id%22%3Anull%2C%22transferOutAccountsStatus%22%3Anull%2C%22transaction%22%3A%7B%22id%22%3A%221018844053740998656%22%2C%22status%22%3A1%2C%22createDateTime%22%3Anull%2C%22payDateTime%22%3A1531746326276%2C%22authToken%22%3A%22TGT-8997191-CPK9DxNmeM2qaovwaALIt4PRyWtfbNzXWD2DrIbKGfbRNLhceb-my.wanfangdata.com.cn%22%2C%22user%22%3A%7B%22accountType%22%3A%22Group%22%2C%22key%22%3A%22hzkjdx%22%7D%2C%22transferIn%22%3A%7B%22accountType%22%3A%22Income%22%2C%22key%22%3A%22ThesisFulltext%22%7D%2C%22transferOut%22%3A%7B%22GTimeLimit.hzkjdx%22%3A30.0%7D%2C%22turnover%22%3A30.0%2C%22productDetail%22%3A%22degree_Y3226485%22%2C%22productTitle%22%3Anull%2C%22userIP%22%3A%22115.156.143.62%22%2C%22organName%22%3Anull%2C%22memo%22%3Anull%2C%22webTransactionRequest%22%3Anull%2C%22signature%22%3A%22GtvO5lpo57sLeaKsI%2Fn5ykDgVD8FtLVwDKU0WXAqYzRO9SBFO4KIKl%2FCGeGk5JibCBCJrIjepaJ7%5Cnles0AF234k2k3Vzon%2FQSLWuaSGYLRsL0%2Fh1oMesYADHg1JSIShDZV80wXmnEbs2Lra2jzC%2F%2B51cH%5CnB57jqr0mF1AymgaXO00%3D%22%2C%22delete%22%3Afalse%7D%2C%22isCache%22%3Afalse%7D)（蒙特卡洛定位技术）

[机器人IMU与激光扫描测距传感器数据融合](http://robot.sia.cn/CN/abstract/abstract12478.shtml)

[基于多传感器数据融合的机器人里程计设计与实现](http://kns.cnki.net/KCMS/detail/detail.aspx?dbcode=CJFQ&dbname=CJFD2012&filename=CGJS201201013&uid=WEEvREcwSlJHSldRa1FhdkJkVWI3Nkp5eEFCSmdBY01GZnVFdFgrczZwVT0=$9A4hF_YAuvQ5obgVAqNKPCYcEjKensW4ggI8Fm4gTkoUKaID8j8gFw!!&v=MDAwNDFyQ1VSTEtmWU9kcEZDbmhXci9OSmlyQmZiRzRIOVBNcm85RVo0UjhlWDFMdXhZUzdEaDFUM3FUcldNMUY=)（归一化特征值加权）

[基于全景视觉与里程计的移动机器人自定位方法研究](http://robolab.sjtu.edu.cn/kindeditor/Upload/file/20170830/20170830163343_0805.pdf)

[基于不确定性分析的视觉里程计优化](http://www.zjujournals.com/eng/CN/abstract/abstract11697.shtml)

------
## License

[![CC0](http://i.creativecommons.org/p/zero/1.0/88x31.png)](http://creativecommons.org/publicdomain/zero/1.0/)
