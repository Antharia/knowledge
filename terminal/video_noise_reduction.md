# How to reduce the background noise of your screencast video ?

## Extract audio from a video

    ffmpeg -i my_video_file.mkv -vn audio_output.wav  

-vn means *no video*.

## Calculate an audio profile

    sox output.wav -n trim 0 3 noiseprof my_video.noise-profile

Use only the first three seconds of your file to analyse your background noise.

## Reduce noise

    sox output.wav cleaned.wav noisered my_video.noise-profile 0.3

0.3 is the amount of noise reduction. Default is 0.5. Higher numbers will alter your audio quality and remove wanted components. Experiment with this parameter and find the best result.

## Replace audio of your video with your cleaned one

    ffmpeg -i my_video_file.mkv -i cleaned.wav -c:v copy -c:a aac -map 0:v:0 -map 1:a:0 final.mkv

-c with ffmpeg select an encoder. So -c:v select video, -c:a select audio, and -map allows to select the stream, here the first one of each file.
