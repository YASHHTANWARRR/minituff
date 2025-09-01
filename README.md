## Robot Package Template

This is a GitHub template. You can make your own copy by clicking the green "Use this template" button.

It is recommended that you keep the repo/package name the same, but if you do change it, ensure you do a "Find all" using your IDE (or the built-in GitHub IDE by hitting the `.` key) and rename all instances of `Minituff` to whatever your project's name is.

Note that each directory currently has at least one file in it to ensure that git tracks the files (and, consequently, that a fresh clone has direcctories present for CMake to find). These example files can be removed if required (and the directories can be removed if `CMakeLists.txt` is adjusted accordingly).

My intake 
For gazeboo the urdf files are necessary as they gives the information about the stucture of the robot.
The splitted urdf files are then combined by xacro into a single processed urdf file called the /robot_sate_publisher which gives the urdf data available on the /robot_description while broadcasting them on the appropiate transforms(/tf).If they are any joints that can move then the robot state publisher,it will see the input values from /joint_states.For our intial testing we can use the /joint_publisher_gui to fake those values.

All of this is then wrapped in a launch file and run it.

<img width="1258" height="667" alt="image" src="https://github.com/user-attachments/assets/356a30f2-0a35-427e-80fd-0b732d704b49" />

