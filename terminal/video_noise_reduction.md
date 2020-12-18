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
