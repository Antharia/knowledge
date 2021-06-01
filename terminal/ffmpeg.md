# FFMPEG

## Single file conversion example

    ffmpeg -i example.mkv -c copy example.mp4

## Merging audio file with video file

    ffmpeg -i video.mp4 -i audio.wav -c copy output.mkv
    
## Add audio fade out to a video
    
st=XX, XX is the starting point in seconds

d=X, X is the duration in seconds

    ffmpeg -i output.mkv -af "afade=t=out:st=XX:d=X" output2.mkv
    
## Capture screen on Linux

    ffmpeg -video_size 1280x800 -framerate 24 -f x11grab -i :0.0 output.mp4
