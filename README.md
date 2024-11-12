# Gazebo Harmonic Simulation Example

This is a simple example of using gazebo harmonic for ROS2 Humble Navigation stack.

## Pre-requisites

- You should already have Gazebo Harmonic installed, consult [Gazebo Harmonic with ROS 2 Humble, Iron or Rolling](https://gazebosim.org/docs/latest/ros_installation/#gazebo-harmonic-with-ros-2-humble-iron-or-rolling-use-with-caution)
- Install Slam Toolbox ```sudo apt install ros-humble-slam-toolbox```
- Install Nav2 [https://docs.nav2.org/getting_started/index.html#installation](https://docs.nav2.org/getting_started/index.html#installation)

## Running the simulation

- Clone this repository into your workspace
- Build the workspace
- Source the workspace

## Running Basic Simulation

Run the following command to launch the simulation

```bash
ros2 launch gazebo_garden_simulation_example sim.launch.py 
```

Wait until the bridge is launch and in another terminal, run the following command to launch teleop

```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```

## Running SLAM Simulation

Run the following command to launch the simulation

```bash
ros2 launch gazebo_garden_simulation_example sim.slam.launch.py
```

Wait until the bridge is launch and in another terminal start SLAM

```bash
ros2 launch gazebo_garden_simulation_example slam.launch.py
```

Wait until the map is built and in another terminal, run the following command to launch teleop to start mapping

```bash
ros2 run teleop_twist_keyboard teleop_twist_keyboard
```

## Running Navigation Simulation

Run the following command to launch the simulation

```bash
ros2 launch gazebo_garden_simulation_example sim.nav.launch.py
```

Wait until the bridge is launch and in another terminal start Navigation

```bash
ros2 launch gazebo_garden_simulation_example nav.launch.py
```

## Other Information

Modified version of [tugbot](https://app.gazebosim.org/MovAi/fuel/models/Tugbot) is used in the simulation. The modified version is available in the `models` folder.
