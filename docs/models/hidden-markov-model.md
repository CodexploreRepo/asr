# Hidden Markov Model

## Introduction

- **Speech recognition** engines usually require 2 basic components in order to recognize speech.
  - One component is an **acoustic model**, created by taking audio recordings of speech and their transcriptions and then compiling them into statistical representations of the sounds for words.
    - **Hidden Markov Model (HMM)** is one most common type of acoustic models.
  - The other component is called a **language model**, which gives the probabilities of sequences of words.
    - Language models are often used for dictation applications. A special type of langauge models is regular grammars
