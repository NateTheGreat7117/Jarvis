# Jarvis
A virtual assistant resembling Iron Man's Jarvis.

## Speech Recognition
A pre-trained wav2vec model was finetuned on 4000 samples of my own speech data to better fit my voice.

### Voice Classification
In order to allow Jarvis to only respond to my voice, I made a voice classifier using samples from the dataset I created for the speech recognition model and speakers in Mozilla's speech dataset. The architecture is a convolutional network that takes a spectrogram as the input.

## Chatbot
A seq2seq transformer was built with a pre-trained Bert encoder and a decoder with custom attention layers. It was trained on over 500 lines of conversations with an AI assistant that I wrote, along with some interactions between Jarvis and Tony Stark from Iron Man.

### Voice Target Recognition
I did not want Jarvis to respond when I was not talking to him, so I had to create a simple dataset that contained samples of sentences that I would say to Jarvis and samples I would say to someone in real life. I used ChatGPT to get most of these data samples but I also made some that were better suited to my specific need.

## Speech Generation
An implementation of coqui-ai's text-to-speech was used to clone Jarvis' voice from the movie.
