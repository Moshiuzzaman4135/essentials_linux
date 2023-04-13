# FFMPEG
- ### To see information about a video
```
ffprobe video.mp4
```
> This show information like duration, bitrate , fps , resolution etc. of a video file
- ### To capture the video of a rtsp feed and save it in a file
```
ffmpeg -i rtsp://url -vcodec copy output.mp4
```
- ### To capture the video of a rtsp feed and save it in a file with tcp transport
```
ffmpeg -rtsp_transport tcp -i rtsp://url -vcodec copy output.mp4
```
- ### Capture the video of a rtsp feed and save it in segments of desired length
```
ffmpeg -rtsp_transport tcp -i rtsp://url -c copy -f segment -segment_time 120 output_file_pattern_%d.mp4
```
> Here 120 is the duration of 2 minutes. So every video will be 2 minutes long
- ### Change frame rate
```
ffmpeg -i input.mp4 -filter:v fps=30 output.mp4
```