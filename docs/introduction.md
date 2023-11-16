# Introduction to Audio

## What is Sound & Audio ?

### Sound

- Sound has properties: Frequency, Amplitude (Intensity DB/Power) & Direction
- **Sine Wave**: $y(t) = A\sin(2 \pi ft + \phi)$
- **Wavelength** $λ$ can be measured between any two points with the same phase

<p align="center">
<img src="../assets/img/sine_wavelength.png" width=250 /></p>

- Frequency & Amplitude
  - Higher frequency &#8594; Higher Sound
  - Larger amplitude &#8594; Louder
  <p align="center">
  <img src="../assets/img/freq-amplitude.png" width=350 /></p>

### Audio

- Audio is the electronic representation of sound
- Audio Frequency.

  - Range: 20 to 20kHz
  - Describes the differences of wavelength - High Frequency &#8594; Short Wavelegth - Low Frequency &#8594; Long Wavelegth
    <p align="center">
    <img src="../assets/img/wavelength_frequency.png" width=350 /></p>

- `Intensity` (DB/Power): describes the amplitude (height) of the wave.
<p align="center">
  <img src="../assets/img/intensity.gif" width=250 /></p>

- `Sample Rate` (Resolution of Audio): how the computer reads in the audio file.
  - Range: 16kHz, 44.1kHz (take 44,000 samples or measurements per second) &#8594; The more sample per second get, the higher quality captured
- `Waveform`: samples over the time
- `Spectrogram`: a visual way of representing the signal strength, or “loudness”, of a signal over time at **various** frequencies present in a particular waveform.

  - We can convert the **waveform** to **Spectrogram** (image) &#8594; can classify sound using the same technique when classifying the images

  <p align="center">
  <img src="../assets/img/spectrogram.png" width=400 /></p>

  - _x-axis_: time
  - _y-axis_: frequency in Hz
  - _color_: magnitude or amplitude (the brighter the higher in DB)

  <p align="center">
  <img src="../assets/img/waveform_spectrogram_bird.png" width=500 /></p>

## Audio Tasks

### Audio Classification

- Application:
  - **Language Detection**: extremely useful as a preprocessing step for other systems
    - Dataset: [VoxLingua107](https://bark.phon.ioc.ee/voxlingua107/) allows to train language identification models for up to 107 languages.
  - **Command Recognition**: Command recognition or keyword spotting classifies utterances into a predefined set of commands. This is often done on-device for fast response time. - Dataset: Google Speech Commands dataset, given an input, a model can classify which of the following commands the user is typing: `'yes', 'no', 'up', 'down', 'left', 'right', 'on', 'off', 'stop', 'go', 'unknown', 'silence'
`
  - **Speaker Identification**: to classify the audio of the person speaking. Speakers are usually predefined.
    - Dataset: VoxCeleb1
- Metrics: Accuracy, Recall, Precision, F1
- Pre-trained Model:
  - Wav2Vec2
  - [HuBERT](https://huggingface.co/superb/hubert-large-superb-er)

### Automatic Speech Recognition

- Automatic Speech Recognition (ASR), also known as Speech to Text (STT), is the task of transcribing a given audio to text.
- Datasets:

| Dataset      | Hours                        | Source       | Language Support |
| ------------ | ---------------------------- | ------------ | ---------------- |
| Librispeech  | 1000 hours                   | Audio books  | English          |
| Common Voice | >9000 hours                  | Crowdsourced | multi-language   |
| Vox Populi   | 400k hours of unlabeled data |              | multi-language   |

- Application:
  - **Virtual Speech Assistants**: Many edge devices have an embedded virtual assistant to interact with the end users better.
  - **Caption Generation**: to take audio as input from sources to generate automatic captions through transcription, for live-streamed or recorded videos.
- Metrics: WER (Word Error Rate)
