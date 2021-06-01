# FFMPEG

## Single file conversion example

    ffmpeg -i example.mkv -c copy example.mp4

## Merging audio file with video file

    ffmpeg -i video.mp4 -i audio.wav -c copy output.mkv
