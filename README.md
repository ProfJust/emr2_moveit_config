# emr2_moveit_config

usage
$ ros2 launch emr2_moveit_config demo.launch.py


Bug-Solver
-------------

[ERROR] [launch]: Caught exception in launch (see debug for traceback): 'capabilities'

=> https://github.com/moveit/moveit2/issues/2734


.setup
---------
GitHub speichert keine Versteckten Dateien, daher
für die Nutzung der Moveit-Setup-Assistenten vorher die GitHub-Datei 
setup_assistant  in .setup_assistant umbenennen

ur.urdf  / ur5x
-----------------
Das Default im File ur.urdf.xacro  auf ur3e, ur3 oder ur5e setzen

Zeile 10:   <xacro:arg name="ur_type" default="ur5x"/>

=>   <xacro:arg name="ur_type" default="ur3e"/>


Dann das urdf-File im Ordner /home/oj/ur3_ws/src/Universal_Robots_ROS2_Description/urdf/ur.urdf  
mit dem Xacro-Befehl erzeugen:

$ cd ~/ur3_ws/src/Universal_Robots_ROS2_Description/urdf
$ xacro ur.urdf.xacro name:=ur > ur.urdf 


