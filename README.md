# Alert-Generation-on-Detection-of-Suspicious-Activity-using-Transfer-Learning 🕵️‍♂️ 
ADAG (Activity Detector and Alert Generator) aims to take real-time videos from CCTV as an input and pass it to the CNN model created with the help of transfer learning and detect ‘Shoplifting’, ‘Robbery’ or ’Break-In’ in the store and notify it to the owners as soon as it occurs. Finally the main motive is to provide a system that detects suspicious activities without human intervention and generates alert, thus making a huge revolution in today’s surveillance system.

<img src="https://github.com/OmRajpurkar/Alert-Generation-on-Detection-of-Suspicious-Activity-using-Transfer-Learning/blob/main/videoClassification/Shoplifting.gif" alt="alt text">

## Downloading and Configuring

```
gh repo clone OmRajpurkar/Alert-Generation-on-Detection-of-Suspicious-Activity-using-Transfer-Learning
```

* Download the [model](https://drive.google.com/file/d/1nTohU6YgXZvU155_vccnD2OEkdTW166W/view?usp=sharing) and place it inside ‘videoClassification’ directory.

* Create a new Virtual Environment and Activate it.

* To save the dataset images create a directory named 'data' inside the 'videoClassification' directory. Inside the 'data' directory create 3 sub-directories each for 'Shoplifting', 'Robbery' and 'Break-In'. Store the training images for the respective classes inside those directories.

## Requirements

```bash
$ pip install -r requirements.txt
```

## Training the model

```bash
$ python train.py --dataset data --model model --label-bin label_bin --epochs 80
```

## Detecting ‘Shoplifting’, ’Robbery’, ‘Break-In’ in a Video

```bash
$ python predict_video.py -m model -l label_bin -i /videoClassification/Shoplifting.mp4 -o ShopliftingOutput.avi
```

## Predicting ‘Shoplifting’, ’Robbery’, ‘Break-In’ in Real-time using Webcam

```bash
$ python predict_video_realtime.py -m model -l label_bin -o output
```

## Published Paper

O. M. Rajpurkar, S. S. Kamble, J. P. Nandagiri and A. V. Nimkar, "Alert Generation on Detection of Suspicious Activity Using Transfer Learning," 2020 11th International Conference on Computing, Communication and Networking Technologies (ICCCNT), Kharagpur, India, 2020, pp. 1-7, doi: 10.1109/ICCCNT49239.2020.9225263.

IEEE Xplore Link: https://ieeexplore.ieee.org/document/9225263
