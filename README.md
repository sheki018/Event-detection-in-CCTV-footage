# Event-detection-in-CCTV-footage

## Our idea:

Surveillance videos are able to capture a variety of realistic anomalies. One critical task for law enforcement officers in video surveillance is detecting anomalous events such as knife attacks and chain snatching for investigation. Generally, anomalous events rarely occur as compared to normal activities. Therefore, to alleviate the waste of labor and time, developing intelligent computer vision algorithms for automatic video anomaly detection is a pressing need. The goal of a practical anomaly detection system is to timely signal an activity that deviates normal patterns and identify the time window of the occurring anomaly. Therefore, anomaly detection can be considered as video understanding at a coarse level, which filters out anomalies from normal patterns. Once an anomaly is detected, it can further be categorized into one of the specific activities using classification techniques.


## Our approach:

We propose an anomaly detection algorithm using training videos with weak labels which means that we only know the video-level labels, i.e. a video is normal or contains anomaly somewhere, but we do not know where. To formulate a weakly-supervised learning approach, we resort to multiple instance learning. Specifically, we propose to learn anomaly through a deep MIL framework by treating normal and anomalous surveillance videos as bags and short segments/clips of each video as instances in a bag. Based on training videos, we automatically learn an anomaly ranking model that predicts high anomaly scores for anomalous segments in a video. During testing, a long video is divided into segments and fed into our deep network which assigns anomaly score for each video segment such that an anomaly can be detected. Finally the video which contains the anomaly is identified and the exact time stamp of it is displayed.
Our experimental results show that our MIL method for anomaly detection achieves significant improvement on anomaly detection performance as compared to the state-of-the-art approaches. We provide the results of several recent deep learning baselines on anomalous activity recognition. The low recognition performance of these baselines reveals that our dataset is very challenging and opens more opportunities for future work.

