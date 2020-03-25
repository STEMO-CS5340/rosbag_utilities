

## Example:

### bagmerge.py

This tool helps to merge two bags with the specified topics. Default with --lz4 compression
``` bash
rosrun rosbag_utilities bagmerge.py -o out.bag -t /zed/zed_node/left/camera_info,/zed/zed_node/left/image_rect_color,/zedm/zed_node/left/camera_info,/zedm/zed_node/left/image_rect_color 2020-03-22-17-03-58_zed.bag 2020-03-22-17-03-58_mzed.bag
```

### annotator.py
``` bash
rosrun rosbag_utilities annotator.py out.bag /zed/zed_node/left/image_rect_color
```
Key	Description
a	Go forward 1 frame
d	Go back 1 frame
s	Saves timestamp with id 0
w	Saves timestamp with id 1
q	Saves timestamp with id 2
e	Saves timestamp with id 3
z	Saves timestamp with id 4
space	Pauses program
left arrow	Reduce playback speed
right arrow	Increase playback speed
Esc	Quits program

https://github.com/dsgou/rosbag_annotator

### bagimagesnap.py

``` bash
rosrun rosbag_utilities bagimagesnap.py out.bag output /zed/zed_node/left/image_rect_color /zedm/zed_node/left/image_rect_color -t 1584867843.32 1584867847.96 1584867850.99 1584867855.57 1584867858.64 1584867861.74 1584867865.01  1584867867.79 1584867873.03 1584867876.9  1584867881.94 1584867888.75 1584867893.39

```
### rosbag filter "t.secs"

Use annotator.py to locate the range first, then use rosbag filter