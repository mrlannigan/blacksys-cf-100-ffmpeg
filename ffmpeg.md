h3. Overlay Blacksys 2 channel video PIP

```
ffmpeg -i 20160322_171143_I2.avi \
  -ss 10 \
  -filter_complex "[0:1]scale=iw/3:ih/3 [pip]; [0:0][pip] overlay=main_w-overlay_w-30:main_h-overlay_h-60" \
  -profile:v main \
  -level 3.1 \
  -s 1920x1080 \
  -vcodec h264 \
  /tmp/PIP_output1.mp4
```
