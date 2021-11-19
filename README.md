# Topic Latency Test
## Purpose
- The package have both publisher/subscriber to calculate transmittion latency of a short string message.
- It should run on ROS1 noetic
## Usage
- With ROS1 installed, follow below steps:
```bash=
. /opt/ros/noetic/setup.bash
mkdir test_ws
mkdir src
cd src
git clone https://github.com/NTURacingTeam/topic_latency_test.git
cd ..
catkin_make
. devel/localsetup.bash
roscore &
rosrun topic_latency_test tlt_talker &
rosrun topic_latency_test tlt_listener
```
## Result
### Rpi 3B
- Environment: Raspbian/in Docker
- Average latency: 1.0~1.2 ms
- Maximum latency: 13 ms
- Other: the latency didn't affected much under "stress -c 4"
