# SER Evaluation
This repository holds three files, meant to serve as a proof of concept of the following translation pipeline with emotion matching:

1. The file is preprocessed, dividing it into chunks based on pauses, converting into 16 kHz and into mono if necessary;
2. The source audio file containing speech is transcribed and translated, in this case OpenAI Whisper was used;
3. In parallel, the file goes through a speech emotion recognition model to infer the emotion, in this case Emotion2Vec;
4. With the transcription and emotion per chunk, a text-to-speech model capable of emotion synthesis is used go generate speech, in this case Gemini 2.5 Pro Preview TTS.

The result is a translated version of the original file with emotions that roughly match each phrase.
