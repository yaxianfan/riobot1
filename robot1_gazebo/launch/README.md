gazebo_test1_1.launch是加载heightmap和石块和gazebo搭建小车的环境


  <!-- Load the URDF into the ROS Parameter Server -->
  <param name="robot_description"
         command="$(find xacro)/xacro --inorder '$(find robot1_description)/urdf/robot1_base_04.xacro'" />
修改此处可以加载不同的机器人
