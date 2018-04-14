mkdir ws && cd ws

wstool init src https://github.com/samiamlabs/object_recognition_rosinstall/raw/master/ork.rosinstall.kinetic

cd src && wstool update -j8

cd .. && rosdep install --from-paths src -i -y

catkin_make

source devel/setup.bash
