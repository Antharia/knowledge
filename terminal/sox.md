# SOX
SoX - Sound eXchange, the Swiss Army knife of audio manipulation

Concatenate audio files
    sox track1.mp3 track2.mp3 track3.mp3 full_album.mp3
    
Mix audio files
    sox -m track1.mp3 track2.mp3 track3.mp3 mix.mp3
    
Split an audio file based on silence
    sox input.wav output.wav silence -l 1 0.0 -40d 1 1.0 -40d : newfile : restart
