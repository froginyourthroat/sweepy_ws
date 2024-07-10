# Sweepy Bot

Sweepy Bot is an autonomous mobile robot designed for sweeping tasks. This README provides instructions on how to set up and run the robot stack, SLAM, navigation, joystick control, and custom obstacle detection.

## Getting Started

### Prerequisites

Ensure you have the following installed:
- ROS 2
- Relevant ROS 2 packages and dependencies

### Repository Setup

Clone the repository and navigate to the workspace:

```sh
git clone https://github.com/froginyourthroat/sweepy_ws.git
cd sweepy_ws
colcon build
source install/setup.bash
```

## Launching the Robot

### 1. Robot Stack

Launch the robot stack which includes drivers and sensor nodes:

```sh
ros2 launch sweeper_bot sweepy_launch.py
```

### 2. SLAM

To perform simultaneous localization and mapping (SLAM), use the following command:

```sh
ros2 launch sweeper_bot online_async_launch.py
```

### 3. Navigation

For autonomous navigation, launch the Nav2 stack:

```sh
ros2 launch sweeper_bot navigation_launch.py
```

### 4. Joystick Controller

If you want to control the robot manually using a joystick:

```sh
ros2 launch sweeper_bot joystick_launch.py
```

### 5. Custom Obstacle Detection

Launch the custom obstacle detection node to enhance the robot's awareness:

```sh
ros2 launch sweeper_bot obstacle_detection_launch.py
```

## Configuration Files

### `sweepy_launch.py`
Contains configurations for initializing the robot stack, including sensors and drivers.

### `online_async_launch.py`
SLAM setup for creating and updating the map in real-time.

### `navigation_launch.py`
Nav2 setup for path planning and autonomous navigation.

### `joystick_launch.py`
Joystick controller setup for manual robot control.

### `obstacle_detection_launch.py`
Custom node configuration for obstacle detection.

## Usage

### Running the Full Stack

To launch the entire robot stack, SLAM, and navigation:

```sh
ros2 launch sweeper_bot sweepy_launch.py
ros2 launch sweeper_bot online_async_launch.py
ros2 launch sweeper_bot navigation_launch.py
```

### Manual Control

For manual control with a joystick, use the joystick launch file:

```sh
ros2 launch sweeper_bot joystick_launch.py
```

### Custom Obstacle Detection

Enhance obstacle detection by launching the custom node:

```sh
ros2 launch sweeper_bot obstacle_detection_launch.py
```

## Troubleshooting

### Common Issues

- **Connection Issues**: Ensure all hardware is properly connected and configured.
- **Dependency Errors**: Make sure all dependencies are installed and sourced.

### Support

For support, open an issue on the [GitHub repository](https://github.com/froginyourthroat/sweepy_ws/issues).

## Contributing

We welcome contributions! Please see our [contributing guidelines](https://github.com/froginyourthroat/sweepy_ws/blob/main/CONTRIBUTING.md) for more details.

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/froginyourthroat/sweepy_ws/blob/main/LICENSE) file for details.
