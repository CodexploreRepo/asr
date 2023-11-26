# Daily Knowledge

## Day 1

- Speaker Recognition vs Speech Recognition
  - Speaker recognition is to ascertain the identity of a person using his or her voice. We are interested in "who is speaking"
  - Speech recognition aims to ascertain "what was spoken."
- **Speech recognition** engines usually require 2 basic components in order to recognize speech.
  - One component is an **acoustic model**, created by taking audio recordings of speech and their transcriptions and then compiling them into statistical representations of the sounds for words.
    - **Hidden Markov Model (HMM)** is one most common type of acoustic models.
  - The other component is called a **language model**, which gives the probabilities of sequences of words.
    - Language models are often used for dictation applications. A special type of langauge models is regular grammars

### Audio Signal Capture (Analog to Digital Converter - ADC)

- Step 1: capture the sound using the microphone &#8594; Graph (x-axis: Time (s); y-axis: Amplitude (dB))
- Step 2: sample the captured graph with the sampling rate to get the digital signal
- Step 3: use fast fourier transform &#8594; Spectrogram (x-axis: Time (ms), y-axis: Frequency (kH), and the color to represent the energy of the sound (dB))
