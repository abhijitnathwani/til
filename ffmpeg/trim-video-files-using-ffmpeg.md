# Trim video files using `ffmpeg`

`ffmpeg -i input.mp4 -ss 01:19:27 -to 02:18:51 -c:v copy -c:a copy output.mp4`

This will cut out the section from about 1h19min to 2h18min, and will only take a few seconds to run. If you instead want to specify a fixed duration, you can use:

`ffmpeg -i input.mp4 -ss 00:01:10 -t 00:01:05 -c:v copy -c:a copy output.mp4`

This will extract 1min5sec starting from 1min10sec in the file.

[Source](https://www.arj.no/2018/05/18/trimvideo/)
