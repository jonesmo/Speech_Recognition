<br />
<p align="center">
  <h3 align="center">Speech Command Recognition with CNNs and Librosa</h3>

  <p align="center">
    Built and methodically optimized 16 neural networks to identify among 34 spoken commands, considering both accuracy and efficiency. Built upon existing models used in speech recognition; final model outperformed that by researchers at the University of Montreal with an accuracy of 83%, strong recall and precision for all labels, and a reduced feature space which used modest computational resources to train.  Useful wherever single-word spoken commands must be understood by devices or smart objects including autonomous vehicles.
    <br />
    <br />
    <a href="https://colab.research.google.com/drive/1sgwQrpbOW9BUXkTtmtUHOVnZy8gF3xyp?usp=sharing">View Notebook</a>
  </p>
</p>


<!-- ABOUT THE PROJECT -->
## About The Project

I chose to tackle this project because of my ongoing interest in audio information retrieval and my desire to learn the Librosa Python library.


### Built With

* []() TensorFlow/Keras
* []() Librosa
* []() Numpy
* []() <a href="https://ai.googleblog.com/2017/08/launching-speech-commands-dataset.html">Audio data</a> from the Google AIY and TensorFlow teams


## Feature Engineering

The dataset consisted of 104,000 crowdsourced audio files of single-word spoken commands.  Two datasets were derived from this: one, the audio data itself, resampled to 8000 Hz and all samples shorter than 1 second dropped.  The second consists of an array of MFCCs (Mel frequency cepstrum coefficients) extracted from each audio file.  Each dataset was fed into a series of models, with the hypothesis that MFCCs would produce results almost as accurate and less computationally demanding than models requiring the full audio data.


## Model Building

Three basic structures for neural networks were based on research by data scientists at University of Montreal, Stanford, Cornell, and independent professionals.  These were then optimized methodically for a total of 16 models; the summary of these models can be found <a href="https://docs.google.com/spreadsheets/d/14gmZQ5KOuHXWG56O5N_PXGECjSVSUjJr0C5NGMiOcT8/edit?usp=sharing">here</a>.

The favored model has a training accuracy of 84% and testing accuracy of 83%, avoiding overfitting, and only requires MFCCs as input, resulting in a simpler, more computationally effective model than that used by the University of Montreal researchers and with higher accuracy.  The model has high precision and recall for all 34 of the labels identified.  Pairs of words most often (but still not often) confused by the model include: three/tree, go/no, four/forward, and up/off.


## Future Work

The next steps including combining RNNs with CNN layers effectively as some models have successfully done, adding audio features to MFCCs that may increase accuracy while not dramatically increasing training time, and considering either adding or eliminating background noise to the audio samples.
