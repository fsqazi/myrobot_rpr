# myrobot_rpr
My tiring and motivating journeyy through Ros2. Honestly it was a learning experience.

When u import my folder which is mytest_ws.
colcon build it
and try to run
ros2 launch myrobot_rpr display.launch.py
an RVIZ window will show up with the moving control gui 
u can change the levels and see if it works.
IF IT GIVES MESHES NOT FOUND IN UR COMMANDLINE.
JUST OPEN MY URDF file which is in scr/myrobot/rpr/urdf
and go thorught the meshes part and give it ur location where the meshes are placed now.
IT WILL WORK.
WHEN IT IS WORKING NOW RUN THE 
ros2 launch myrobot_rpr_moveit_config demo.launch.py
it will load the model in rviz 
HERE U CAN PLAN ANY MOTION OF MY ROBOT AND IT CAN PERFORM IT.
Now in 2nd terminal run
ros2 launch myrobot_rpr_moveit_config mygazebo.launch.py
MY MODEL WILL OPEN UP IN GAZEBO.

PROBLEMS FACED:
I was able to import the urdf from solidworks (which honestly is a tiring process)
Then the urdf is broken at this point and it doesnt run in the moveit assistant to fix it we have to open urdf files and where ever there is an integer we have to convert it to the float in order to correct it.
When it is done then colcon build it and open the moveit_setup_assistant.launch.py in the folder and load the urdf. IT WILL LOAD :)
Config the robot and generate the folder the folder should have the same name like
myrobot_rpr was my folders name and now the new folder should have the name "myrobot_rpr_moveit_config" it doesnt work if the name is changed NOTE THIS.
Now go in this new folder and if we try to run the demo.launch.py file it doesnt work.
WE HAVE TO FIX THE XACRO FILES AND OTHER FILES WHICH ARE IN THE CONFIG TO MAKE IT WORK.
again do the int -> float and then run it again. it will work.
NOW THERE IS NO GAZEBO LAUNCH FILE BY DEFAULT AND WE HAVE TO MAKE IT FROM SCRATCH I CREATED IT AND ITS NOW IN MY LAUNCH FOLDER :)

THANKS FOR THIS EXPERIENCE MADAM! :)
