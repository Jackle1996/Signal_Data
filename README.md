# Signal_Data


## Intro
Content of this repo:
- Data set of 1'840 images which contain one or more signals
- OpenLabeling Software to label the images [OpenLabeling](https://github.com/Cartucho/OpenLabeling)
- test statistic files per 5000 iterations
- notebook which creates train/test split
- notebook which creates graphs bases on test statistic


## Install Packages
``` bash
pip install -r requirements.txt
```


## Classes
[available classes](main/class_list.txt)

## YOLOv3
[used Yolov3 Tiny config](/yolo_v3_config/yolov3-tiny-custom.cfg)


## Statistic
True Positive = Signals which got predicted right. Example: we have a 6, we predict a 6 which is true

False Positive = Signals which got predicted wrong. Example: we have a 6, but we predict a 4 which is wrong

False Negative = Signals which weren't detected at all

### Summary
Most important graph!
![summary](/graphs/summary.png)

The quite large amount of false positives comes from double predictions on single signals:

Example: We have a signal info-6, we predict ...

probability | class |
------------- | ------------- |
80 % | info-6 |
50 % | info-9 |

In this example, it is clear that 6 is the correct answer.
The second answer (50% info-9) has a high enough probability, so it adds to the false positives.


### Start signal
![start](/graphs/start.png)

### White/Black info signals
info signals are the higher ones
![white-info-1](/graphs/white-info-1.png)
![white-info-2](/graphs/white-info-2.png)
![white-info-3](/graphs/white-info-3.png)
![white-info-4](/graphs/white-info-4.png)
![white-info-5](/graphs/white-info-5.png)
![white-info-6](/graphs/white-info-6.png)
![white-info-7](/graphs/white-info-7.png)
![white-info-8](/graphs/white-info-8.png)
![white-info-9](/graphs/white-info-9.png)
![black-info-1](/graphs/white-info-1.png)
![black-info-2](/graphs/white-info-2.png)
![black-info-3](/graphs/white-info-3.png)
![black-info-4](/graphs/white-info-4.png)
![black-info-5](/graphs/white-info-5.png)
![black-info-6](/graphs/white-info-6.png)
![black-info-7](/graphs/white-info-7.png)
![black-info-8](/graphs/white-info-8.png)
![black-info-9](/graphs/white-info-9.png)

### White/Black stop signals
stop signals are the lower ones
![white-stop-1](/graphs/white-stop-1.png)
![white-stop-2](/graphs/white-stop-2.png)
![white-stop-3](/graphs/white-stop-3.png)
![white-stop-4](/graphs/white-stop-4.png)
![white-stop-5](/graphs/white-stop-5.png)
![white-stop-6](/graphs/white-stop-6.png)
![white-stop-7](/graphs/white-stop-7.png)
![white-stop-8](/graphs/white-stop-8.png)
![white-stop-9](/graphs/white-stop-9.png)
![black-stop-1](/graphs/white-stop-1.png)
![black-stop-2](/graphs/white-info-2.png)
![black-stop-3](/graphs/white-stop-3.png)
![black-stop-4](/graphs/white-stop-4.png)
![black-stop-5](/graphs/white-stop-5.png)
![black-stop-6](/graphs/white-stop-6.png)
![black-stop-7](/graphs/white-stop-7.png)
![black-stop-8](/graphs/white-stop-8.png)
![black-stop-9](/graphs/white-stop-9.png)
