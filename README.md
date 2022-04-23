# Tell the Time Networks
Using a collection of images of analog clocks accompanied by the respective labels a variety of CNNs have been produced with the aim to predict the time of these images. Due to the cyclic nature of time as a feature, the calculation of the error between the target value and the prediction is not as straightforward as subtracting
the two values. Customized "common sense accuracy" has been used for the evaluation process. For example predicting 11:58 but the target being 00:02 should only calculate an error of 4 minutes.

Implementations involved the following CNNs:
- Regression: neural network with a regression and a single output node for both the hour and minutes
- Classification: There are 12 hours and 60 minutes on an analog clock. Instead of creating classes for every possible combination of hour and minutes (720 total classes), it was decided to experiment with some interval for grouping the minutes by.
- Cyclic encoding: Time is cyclic in nature, since it repeats its pattern in a circular motion. Input of CNN (time) has been cyclic encoded (sin and cos of both hour and minutes). 
-Multihead models: Final approach involved a multi-head neural network, with two different heads for the hours and minutes prediction (hour classified and minutes cyclic encoded).

### Collaborators
- [Andreas Paraskeva](https://www.linkedin.com/in/andreasparaskeva/)
- [Pol Mor Puigventós](https://www.linkedin.com/in/pol-mor/)