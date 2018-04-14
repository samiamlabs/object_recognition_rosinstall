mkdir ws && cd ws
wstool init src https://raw.github.com/wg-perception/object_recognition_core/master/doc/source/ork.rosinstall.kinetic.plus
cd src && wstool update -j8
cd .. && rosdep install --from-paths src -i -y
catkin_make
source devel/setup.bash
