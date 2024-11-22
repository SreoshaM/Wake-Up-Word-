# Wakeup-Word
It's just a simple Wakeup Word with great accuracy. The audio data are collected by using sounddevice framework. Librosa has been used to preprocess and extract the MFCC (Mel Frequency Cepstrum Coefficient) features from the audio samples collected so far. The data is then fed to the Neural Network for training. We need a mic in order to provide best accuracte practices.  
## Collecting data
By running the prepare.py you can collect 100 wakeup words and 100 noises, since it's abinary classifiaction problem.
```bash
python prepare.py
```
## Preprocessing and training
The collected data are then preprocessed. The pre-processing has been done by using librosa library as mentioned before. 
```bash
python preprocess.py
```
then
```bash
python train.py
```
## Prediction and inference
This is a real-time prediction. During the prediction, whatever voice (2 secs duration) is collected from the user is stored in a temporary wavefile "predict.wav" and that wavfile is passed to our model to predict whether it's a wakeup word or not.
```bash
python inference.py
```