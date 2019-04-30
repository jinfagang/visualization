# visualization

visualization package for ROS. There are plenty of messages defined by us hard to visualized in rviz. So there visualization will gonna help. We support message like:

- 3D BoundingBox with text;
- Trajectory in 3D space;

Note that, we implemented all effect using Marker but not rviz plugin, so it will has a full efficiency.
Here is the effect of visualizer:

<p align="center">
<img src="https://s2.ax1x.com/2019/04/30/E8qy7Q.md.png" />
</p>

You can toggle to show:

- box;
- box with edges;
- model;
- centroids;
- label;


## Install

Just clone to your workspace, and launch it using:

```xml
 <node pkg="detected_objects_visualizer" type="visualize_detected_objects" 
    name="cluster_detect_visualization_01" output="screen" ns="/dummy">
        <param name="objects_src_topic" value="/dummy/detected_obstacles" />
        <param name="objects_markers_topic" value="/dummy/detected_obstacles_markders" />
        <param name="color_alpha" value="0.6" />
        <param name="label_color" value="255.,0.,255.,0.9" />
</node>
```

Set the in-topic and out-topic, then everything is done.

## Copyright

this package written by Jin Fagang, all rights reserved.