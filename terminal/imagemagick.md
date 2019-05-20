# ImageMagick
## resize
Resize will fit the image into the requested size.
It does NOT fill, the requested box size.
> convert dragon.gif    -resize 64x64  resize_dragon.gif

Ignore Aspect Ratio ('!' flag)
> convert dragon.gif    -resize 64x64\!  exact_dragon.gif

Only Shrink Larger Images ('>' flag)
> convert dragon.gif    -resize 64x64\>  shrink_dragon.gif
