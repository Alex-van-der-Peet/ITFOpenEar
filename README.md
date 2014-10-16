itf_open_ear
==========

This package launches a talker which instantiates an audio processor from the modified ros_open_ear package and publishes the detected emotions on /affectPub and /emoPub.

Prerequisites
-------------
See the geni-lab/ros_open_ear package for instructions on how to install that.

If you are having trouble getting your audio input device to work, try getting the latest version of PortAudio at http://www.portaudio.com/download.html (pa_stable_v19_20140130.tgz worked for us). Unpack it, make, sudo make install.

You'll also have to copy the models and config files from where you installed ros_open_ear. Assuming ~/ros_open_ear for that and ~/catkin_ws/src/itf_open_ear for this package:

cp -R ~/ros_open_ear/config ~/catkin_ws/
cp -R ~/ros_open_ear/models ~/catkin_ws/

And you'll have to run catkin_make to compile itf_open_ear of course.

Usage
-----
To run (from the root of your catkin workspace)

rosrun beginner_tutorials talker -C config/emobase_live4.conf

To check if it's working:

rostopic echo /emoPub

Notes
-----
None.
