# Image Magick Tricks

## Resize image

```
convert dragon_sm.gif    -resize 64x64  resize_dragon.gif
convert dragon_sm.gif    -resize 50% resize_dragon.gif
```

## Compress image

```
convert -strip -interlace Plane -gaussian-blur 0.05 -quality 85% source.jpg result.jpg
```

## Make image grayscale

```
convert <img_in> -set colorspace Gray -separate -average <img_out>
```