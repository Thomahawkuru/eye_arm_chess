# eye_arm_chess (Thomas Edit)
Welcome to de README of the eye_arm_chess repository! First an introduction on what the program does will be provided, next the installation steps will be given and last the code-structure will be explained.

The goal of the program is to connect a Eyelink 100+ eyetracker to a robotic arm of Franka Emica Panda. This is done via a chess program that first lets you input a move via the eyetracker. Than it sends the move to the robotic arm to be executed. A camera-recognition has also been implemented that is able to recognize legal moves on the chess board and show them to the person behind the eyetracker.

## INSTALLATION GUIDE

The chessprogram is implemented in four files. First there are two files for the board and the pieces, called board.py and pieces.py. The special rules of the chessgame are in rules.py. Finally Window.py arranges the gameflow and sends and gets messages from the different instruments. The Connect.py connects the program together with the eyetracker, together with the program CalibrationGraphicsPygame.py file, which was provided by the manufacturer together with the fixationWindow_fastSamples, which contains an example, but is not used in the program. To send moves to the robotic arm the file move_cartesian is used. Furthermore there are a couple of helper files to test with the robot, most importantly pose_recorder, which records exactly which position the robotic arm currently has. Finally the file that is connected to the camera is board_recognition.py, a file which consists for a big part of code from a research project from Washington university in St. Louis (https://classes.engineering.wustl.edu/ese205/core/index.php?title=CV_Chess).

## Software Requirements
- [Franka_ros](https://github.com/frankaemika/franka_ros.git)
- [Panda_moveit_config](https://github.com/ros-planning/panda_moveit_config.git)
- [SR Research Eylink Developers Kit](https://www.sr-support.com/showthread.php?tid=13)
- [Pylink](https://www.sr-support.com/thread-48.html) via propiatary install file
- [Pygame](https://www.pygame.org/wiki/GettingStarted) via pip
