# SOX
SoX - Sound eXchange, the Swiss Army knife of audio manipulation
## 1-liners
Split an audio file based on silence
> sox input.wav output.wav silence -l 1 0.0 -40d 1 1.0 -40d : newfile : restart
