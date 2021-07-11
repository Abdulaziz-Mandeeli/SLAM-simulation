# SLAM-simulation
المهمة الثالثة لتدريب الاساليب الذكية

خطوات تنفيذ المهمة

اولا:

نثبت الادوات الازمة لعمل المحاكاة باستعمال الاكواد التالية

	sudo apt-get install ros-melodic-diff-drive-controller
	sudo apt-get install ros-melodic-amcl
	sudo apt-get install ros-melodic-gmapping
	sudo apt-get install ros-melodic-navigation
	
ثانيا:

نخلق ورك سبيس باستعمال الاكواد التالية

	mkdir -p 2DAutoSlambot/src
	cd 2DAutoSlambot
	catkin_make
	cd src
	catkin_create pkg gslambot
	cd gslambot
	
![image](https://user-images.githubusercontent.com/85806841/125194022-19a25300-e258-11eb-9326-14e2113e1f1e.png)


ثالثا:

نعمل نسخ للباكج باستعمال الكود 
	
	git clone https://github.com/YuCodes/2DAutoSlambot/edit/master/README.md

رابعا:

لتشغيل الباكج نستعمل الاكواد التالية

	roslaunch gslambot gmaprobot.launch model:=path to the /urdf/gmapbot.xacro file
	roslaunch gslambot move_base.launch
	
![image](https://user-images.githubusercontent.com/85806841/125194112-86b5e880-e258-11eb-8168-e1d5201b5e86.png)
![image](https://user-images.githubusercontent.com/85806841/125194127-a51be400-e258-11eb-9d03-da32e275ef2b.png)


خامسا:

وفي النهاية نحتاج لحفظ الخريطة باستعمال الكود

	$ rosrun map_server map_saver -f ~/map
