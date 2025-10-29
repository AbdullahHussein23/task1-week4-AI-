# task1-week4-AI-

1-ندخل على موقع the construct ونفتح مشروع جديد ثم نلصق ال Dependencies التالية اللي موجودة في github شركة الاساليب الذكية على ال terminal:

    sudo apt-get update && sudo apt-get install -y \

     ros-humble-joint-state-publisher-gui \
     
     ros-humble-gazebo-ros \
     
     ros-humble-xacro \
     
     ros-humble-ros2-control \
     
     ros-humble-ros2-controllers \
     
     ros-humble-joint-state-broadcaster \
     
     ros-humble-joint-trajectory-controller \
     
     ros-humble-controller-manager
     
     ros-humble-moveit \
     
     ros-humble-gazebo-ros2-control


2- لتثبيت ال( git) : sudo apt install git

3-لتثبيت ال (colcon):sudo apt install python3-colcon-common-extensions

4- لتثبيت ال( moveit ): sudo apt install ros-humble-moveit

5-نسوي source لملف ال ( ros2): source /opt/ros/humble/setup.bash   

6- نسوي ملف جديد بإسم ( ros2_ws): mkdir -p ~/ros2_ws/src

7- نفتح الملف للتأكد : cd ~/ros2_ws/src

8- لتحميل ال repositoreis كاملة : git clone https://github.com/smart-methods/Robot_Arm_ROS2.git

9- للرجوع خطوة للوراء: cd ..

10-لبناء ال (colcon) : colcon build

11- نسوي source لل (package) : source ~/ros2_ws/install/setup.bash 

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# بعدها لتشغيل arduinobot_description نلصق :

ros2 launch arduinobot_description display.launch.py

بعد ما يشتغل نقدر نتحكم في حركة ال joints

# و لتشغيل  arduinobot_mc نلصق:

ros2 launch  arduinobot_mc demo.launch.py
     
بعد ما يشتغل نفعل Approx ik solutions عشان نتحكم في النقطة النهائية ثم نفعل collision aware ik عشان الروبوت يتأكد انه ما يتصادم مع اي شيء حوله وبعد ما نحدد النقطة النهائية نضغط plan عشان يحدد كم الزوايا المطلوبة عشان نوصل للنقطة النهائية.
