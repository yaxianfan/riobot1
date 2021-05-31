1.首先将models里的几个文件夹复制到.gazebo/models文件夹下



2.使用roslaunch robot1_gazebo gazebo_test1_1.launch打开模拟环境

3.石头可以调整为动态和静止两种
具体修改为：
打开如下文件
robot1_v2_0717/robot1_gazebo/worlds/test1_1copy.world

    <population name="stone_population1">
      <model name="stone1">
        <include>
          <static>false</static>   //将此句中false改为true，stone2.3.4.5.6同理
          <uri>model://stone1</uri>
        </include>
      </model>
      <pose>-50 0 0 0 0 0</pose>
      <box>
        <size>150 150 0.001</size>
      </box>
      <model_count>20</model_count>
      <distribution>
        <type>random</type>
      </distribution>
    </population>

4.修改不同纹理
.gazebo/models/apollo18copy/materials/textures/texture中有3种不同的纹理，
在完成第1步后，如果需要更换不同的纹理需要112.jpg重命名为11.jpg放置到
.gazebo/models/apollo18copy/materials/textures/11.jpg（11.jpg就是新改的纹理的位置）
注意：在更换不同的纹理的时候需要手动删除
/home/yaxian/.gazebo/paging文件夹里面的东西
要不然加载的还是之前的纹理
