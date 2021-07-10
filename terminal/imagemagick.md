# ImageMagick
## convert
Resize will fit the image into the requested size.
It does NOT fill, the requested box size.

    convert dragon.gif    -resize 64x64  resize_dragon.gif

Ignore Aspect Ratio ('!' flag)

    convert dragon.gif    -resize 64x64\!  exact_dragon.gif

Only Shrink Larger Images ('>' flag)

    convert dragon.gif    -resize 64x64\>  shrink_dragon.gif

Convert to grayscale

    convert image.png -colorspace gray image-grayscale.png

Invert colors

    convert input.png -channel RGB -negate output.png

Turn a video into a gif

    mkdir frames

    ffmpeg -i input.mp4 -vf scale=640:-1:flags=lanczos,fps=10 frames/ffout%03d.png
    
    convert -loop 0 frames/ffout0*.png output.gif

Change quality

    convert high.jpg -quality 80 low.jpg
    
You can get image resolution with _file_ command

    file picture.png

https://imagemagick.org/script/convert.php

