# FFMPEG
## Commands
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
- ### Convert from mkv to mp4
```
ffmpeg -i input.mkv -vcodec copy -acodec copy output.mp4
```
- ### Extract all frames from a video and save them in '.jpg' format in a directory
```
ffmpeg -i input.mp4 thumbs/thumb%04d.jpg -hide_banner
```
- ### Cut video using duration/timestamp
```
ffmpeg -ss 00:05:30 -i input.mp4 -t 00:01:00 -c:v copy -c:a copy output.mp4
```
> ffmpeg -ss start_time -i input.mp4 -t duration_after_start_time_to_cut -c:v copy -c:a copy output.mp4
- ### Add frame number and create another video with frames drawn
```
ffmpeg -i 1.mp4 -vf "drawtext=fontfile=Arial.ttf: text='%{frame_num}': start_number=1: x=(w-tw)/2: y=h-150: fontcolor=black: fontsize=60: box=1: boxcolor=white: boxborderw=5" -c:a copy output.mp4
```
- ### Merge 2 videos side by side and create another output video
```
ffmpeg -i left_video.mp4 -i right_video.mp4 -filter_complex hstack merged.mp4
```
- ### Add text to the top middle of the video and create another output video
```
frsdemo % ffmpeg -i input.mp4 -vf "drawtext=fontfile=/path/to/font.ttf:text='V1':fontcolor=white:fontsize=24:box=1:boxcolor=black@0.5:boxborderw=5:x=(w-text_w)/2:y=10" -codec:a copy output.mp4
```
- ### Add text to the top middle of the video and preview it
```
ffplay -vf "drawtext=fontfile=/path/to/font.ttf:text='V1':fontcolor=white:fontsize=24:box=1:boxcolor=black@0.5:boxborderw=5:x=(w-text_w)/2:y=10" input.mp4
```
- ### Merge multiple ts file into mp4
```
cat segment1_0_av.ts segment2_0_av.ts segment3_0_av.ts > all.ts
ffmpeg -i all.ts -acodec copy -vcodec copy all.mp4
```
## RTSP simple stream server
Download rtsp simple server from [here](https://github.com/aler9/mediamtx/releases)
#### For linux
Download and unzip the file and run the server with the following command
```
./rtsp-simple-server
```
- ### Feed video to rtsp simple server
```
ffmpeg -re -stream_loop -1 -i video.mp4 -c copy -f rtsp rtsp://localhost:8554/mystream
```
### To view/access rtsp feed
```
rtsp://localhost:8554/mystream
```
### To create a Variable time (15 seconds in this case) video from a single image
```
ffmpeg -loop 1 -i input_image.jpg -t 15 -c:v libx264 -pix_fmt yuv420p output_video.mp4
```