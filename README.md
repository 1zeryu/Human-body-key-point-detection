# Human-body-key-point-detection
**Project**: Fitness counter using human key point detection

**Usage:**

```bash
git clone https://github.com/1zeryu/Human-body-key-point-detection.git
```

### Human pose estimation

BlazePose is a lightweight, on-device single person-specific human pose estimation model.

![1659335565937](img/1659335565937.png)

Paper:  [2006.10204v1.pdf (arxiv.org)](https://arxiv.org/pdf/2006.10204v1.pdf) 

you can find the code at  [Human-body-key-point-detection/models at master · 1zeryu/Human-body-key-point-detection (github.com)](https://github.com/1zeryu/Human-body-key-point-detection/tree/master/models) 

### Mediapipe

In this project, I am calling the already trained BlazePose model from mediapipe for **human keypoint detection**.

*You can configure the required environment by*

```python
!pip3 install mediapipe==0.8.7.4 opencv-python numpy --upgrade --user -i http://mirrors.aliyun.com/pypi/simple/ --trusted-host mirrors.aliyun.com
```

You can click on the following links for more information:  [Pose - mediapipe (google.github.io)](https://google.github.io/mediapipe/solutions/pose) 

You can also quickly learn how to detect key points in the human body by looking at my tutorial:  [Human-body-key-point-detection/tutorial at master · 1zeryu/Human-body-key-point-detection (github.com)](https://github.com/1zeryu/Human-body-key-point-detection/tree/master/tutorial) 

But I recommend watching the video for more information: https://www.bilibili.com/video/BV1dL4y1h7Q6?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click

### Movement classification
For common exercise movements such as squats and push-ups, one up and one down is the completion of one movement, and we need to train a classifier to identify whether the stance is up or down at this point.

A common approach is to use the kNN algorithm. You can click on this URL to read the relevant code:  [Human-body-key-point-detection/SquatCounter.ipynb at master · 1zeryu/Human-body-key-point-detection (github.com)](https://github.com/1zeryu/Human-body-key-point-detection/blob/master/models/SquatCounter.ipynb) 

The code here needs to be run using **Google's colab**, and you can add the required toolkit with the following code.

```python
!pip install pillow==8.1.0
!pip install matplotlib==3.3.4
!pip install numpy==1.19.3
!pip install opencv-python==4.5.1.48
!pip install tqdm==4.56.0
!pip install requests==2.25.1

!pip install mediapipe==0.8.3
```

### Deploy

I chose to deploy the fitness counter to **Android**,Use Google's Android application template (ML kit):  [Pose Detection  | ML Kit  | Google Developers](https://developers.google.com/ml-kit/vision/pose-detection) 

You need to modify, debug and generate apk file in professional Android development tool - Android Studio:  [Download Android Studio & App Tools - Android Developers](https://developer.android.com/studio) 

<img src="img/1659407360659.png" alt="1659407360659" style="zoom: 33%;" />

### Reference

#### Link

 [TYZQ/graduation_project_2022: 2022毕设（基于 BlazePose 算法的机器人人体姿势识别与模仿）源码 (github.com)](https://github.com/TYZQ/graduation_project_2022) 

[同济子豪兄奇妙编程夜](https://www.bilibili.com/video/BV1dL4y1h7Q6?spm_id_from=333.1007.top_right_bar_window_custom_collection.content.click)

 [(59条消息) 人体姿态识别方案详解_jieqiang3的博客-CSDN博客_人体姿态识别](https://blog.csdn.net/jieqiang3/article/details/122195209) 

 [(59条消息) 基于 KNN 和 人体关键点的动作分类 - Pose classification_炼丹狮的博客-CSDN博客_动作分类器](https://blog.csdn.net/chenpy/article/details/121466383) 

[MediaPipe](https://mediapipe.dev/) 

[Pose Detection  | ML Kit  | Google Developers](https://developers.google.com/ml-kit/vision/pose-detection) 

#### Book

《第一行代码》  -- 郭霖

链接：https://pan.baidu.com/s/1vjiqegf_LRl90xg-vr8gAg 
提取码：idea 
--来自百度网盘超级会员V2的分享

#### Paper

([BlazePose: On-device Real-time Body Pose tracking)](https://arxiv.org/pdf/2006.10204v1.pdf) )  --Valentin Bazarevsky, Ivan Grishchenko, Karthik Raveendran, Tyler Zhu, Fan Zhang, Matthias Grundmann, Google Research