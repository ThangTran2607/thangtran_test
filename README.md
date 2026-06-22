1. Gọi Sa bàn và Xe (Terminal 1)
Bash
cd ~/thang_ws
source install/setup.bash
ros2 launch thang_ugv_pkg spawn_ugv.launch.py

2. Gọi Thuật toán vẽ bản đồ (Terminal 2)
Bash
source ~/thang_ws/install/setup.bash
ros2 launch slam_toolbox online_async_launch.py use_sim_time:=True

3. Gọi Màn hình giám sát RViz2 (Terminal 3)
Bash
source ~/thang_ws/install/setup.bash
ros2 run rviz2 rviz2 --ros-args -p use_sim_time:=true

4. Bật vô lăng lái xe (Terminal 4)
Bash
source ~/thang_ws/install/setup.bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
