# Banknote-Recognition with M032KG
- Recognizing banknotes with neural network
- Using three photoresistors to measure light intensity corresponding to RGB values. (Each photoresistor is covered with a translucent filter : red, green, or blue.)

<img src="https://github.com/user-attachments/assets/4ea6764f-7dda-4cb0-b275-6f67adf0eb6f" width="750">

## Content
* [Device](#device)
* [Physical Circuit Setup](#physical-circuit-setup)
* [Machine Learning](#machine-learning)
* [Operating Principle](#operating-principle)
* [STEPS](#steps)
* [Flow Chart](#flow-chart)
* [DEMO Video (YouTube)](#demo-video-youtube)

## Device
### [NuvoTon NuMaker-M032KG](https://direct.nuvoton.com/tw/numaker-m032kg)
![numaker-m032kg](https://github.com/user-attachments/assets/53c2646d-d427-4818-993f-16b76a3c903f)

## Physical Circuit Setup
![image](https://github.com/user-attachments/assets/07924d79-20af-4fce-878a-5adcfb9e83ce)

## Machine Learning
- Use MLP (Multilayer Perceptron) as the model architecture.

## Operating Principle
### 🎨 Color Sensor
- Most colors can be represented as a combination of Red (R), Green (G), and Blue (B).
- Each photoresistor is covered with a translucent color filter (R, G, or B), allowing it to sense the intensity of that specific color.
- The analog signal generated by the photoresistor is converted into a digital value via the ADC, representing the light intensity of R, G, or B.


## Flow Chart
<img src="https://github.com/user-attachments/assets/c9f31a80-07d1-4316-83b5-332495b21d1b" width="600">

## Steps
1⃣ `Initialization`:\
Perform an initial scan of the ADC values from the three RGB photoresistors to establish the baseline ambient light levels and continuously monitor the ADC.\
2⃣ `Start Detection (Start of Recording)`:\
Occurring significant change about RGB photoresistor values, meaning that a banknote has been inserted and we start recording the variations in RGB intensity.\
3⃣ `Exit Detection (End of Recording)`:\
Second significant change occurred, the banknote has passed through, and the ambient light has returned to the baseline, stop recording and finalize the RGB time-series data.\
4⃣ `Data Resampling`:\
Resample the recorded time-series data to a fixed temporal length to ensure consistency in model input.\
5⃣ `Banknote Recognition`:\
Predicting the denomination of the banknote.\
6⃣ `Result Display`



## DEMO Video (YouTube)
[![IMAGE ALT TEXT HERE](https://img.youtube.com/vi/qb9uLU0ng0Y/0.jpg)](https://www.youtube.com/watch?v=Xpk8Segaels)

