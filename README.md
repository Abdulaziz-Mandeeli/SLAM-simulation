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
	


ثالثا:

نعمل نسخ للباكج باستعمال الكود 
	
	git clone https://github.com/YuCodes/2DAutoSlambot/edit/master/README.md

