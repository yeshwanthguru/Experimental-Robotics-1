# 🕵️ Experimental Robotics - The  ROS-Based Survilance 🤖                                                               

<p align="center">
  <img src="https://user-images.githubusercontent.com/72270080/218885084-5f1795ba-0d94-4278-b860-9c5e90a1a5f7.png" width="80" height="80" alt="Mobile Robot Icon"/>
</p>


<p align="center">
  <a href="https://www.python.org"><img src="https://img.shields.io/badge/language-python-blue.svg"></a>
  <a href="http://wiki.ros.org/noetic"><img src="https://img.shields.io/badge/ROS-Noetic-FF6F00.svg"></a>
  <a href="https://github.com/yeshwanthguru/Experimental-Robotics-1/pulls"><img src="https://img.shields.io/github/issues-pr/yeshwanthguru/Experimental-Robotics-1"></a>
  <a href="https://github.com/yeshwanthguru/Experimental_robotics/blob/main/LICENSE"><img src="https://img.shields.io/github/license/yeshwanthguru/Experimental-Robotics-1"></a>
  <a href="https://github.com/yeshwanthguru/Experimental-Robotics-1"><img src="https://img.shields.io/github/repo-size/yeshwanthguru/Experimental-Robotics-1"></a>
  <a href="https://github.com/yeshwanthguru/Experimental-Robotics-1/commits/main"><img src="https://img.shields.io/github/last-commit/yeshwanthguru/Experimental-Robotics-1"></a>
</p>



🤖 Name: **Yeshwanth Guru Krishnakumar**

🔌 Reg No: **5059111**

📧 Email: **yeshwanth445@gmail.com**

📜 Check out the Experimental_assignment1_Documentation for my latest robotic project:


🤖 [Experimental_assignment1_Documentation](https://yeshwanthguru.github.io/Experimental-Robotics-1/py-modindex.html) 🚀

## 🤖 INTRODUCTION: 🎲

Welcome to my latest ROS project, an investigation-inspired scenario that demonstrates the power of ROS packages in robotics! This project features an interactive scenario like a ontology based survilance robot. Check out the image below for a sneak peek of ROS package:
   
           
## 🧱 SOFTWARE ARCHITECTURE: 🏗️

This project features a robust software architecture that utilizes a range of cutting-edge technologies and methodologies to create a seamless user experience. Check out the diagrams below to see the high-level structure of the system:

### 🔹 UML Diagram: 📊
<br><br>

<br><br>
### 🔹 Sequence Diagram: 🔄
<br><br>
<br><br>
# 🚀 ARCHITECTURE WORKING PROCESS: 🔧

## ROBOT_STATE_MACHINE : 
🤖🗺️ This script is a ROS-based state machine for a robot to navigate through a topological map of an environment. It 📥 loads the ontology map of the environment 🌍, 🤖 initializes the robot's sensors 🎛️, and defines a state machine with three states: Load_Environment 📥, Normal_mode 🏃, and Emergency_mode 🚨.

In Normal_mode state, the robot chooses the next corridor to move 🏃 or switch to Emergency_mode 🚨. In Navigationway state, the robot navigates 🚶 through the selected corridor. In Emergency_mode state, the robot navigates to the nearest emergency location 🚑🚨.

The robot's sensors are instantiated in the main() function, and the state machine is initialized using the StateMachine() class. The transitions between states are defined using the add() and add_transition() methods of the StateMachine class. The script uses the ArmorClient library to manipulate the ontology map of the environment 🧐.

The script also defines a function to load the ontology map from a file 📁 and apply buffered changes to the ontology, and a function to save the ontology file when the script ends 💾. The script uses the rospy library to initialize a ROS node 🌐 and log information 📝. The script uses the smach library to define and execute the state machine 🤖. 📝🏃‍♂️🏥
## 🧠 ROBOT_BRAIN:
🤖 A robot 🤖 is following a plan consisting of random points 🧭. The plan is generated by a Planning Action Server 🗺️, and the robot's movement is controlled by a Controlling Action Server 🕹️. The robot navigates through the plan by reaching each point with a random delay ⏰. The delay is between two values provided as parameters to the Controlling Action Server.

The start and end points of the plan are set using a service called SetPose 📍. The server checks if the points are within the environment limits 🌳. The robot's current position is also set using SetPose 🔍. The system logs messages at each step to keep track of the robot's progress 📝.

The robot is on a mission to explore the environment and reach its destination safely 🚀. It moves through the environment, encountering obstacles and making decisions on the fly. The robot's sensors help it detect the environment and make decisions based on the data 🤖🔬.
## 🔮 ROBOT_BRAIN2:
🤖📨 This script defines a class ActionClientcortex that implements a SimpleActionClient to send and cancel goals to a specified service. It also defines a class sensory1 that acquires locations from a database using ArmorClient, determines the robot's current location 🗺️, chooses a target location based on the robot's position 📍, reachable locations 🚶, and urgency 🚨.

In the working scenario, the robot uses sensory1 to determine its current location and choose a target location 🎯. Then, the ActionClientcortex is used to send a control action to move the robot to the target location 🏃. The robot moves to the target location 🚀, and the process repeats until a stopping condition is met 🛑.

During the execution of the script, the system logs messages to keep track of the robot's progress 📝. The robot's position and the target location are updated at each iteration to ensure the robot reaches the desired location 📍🎯. The urgency 🚨 of the target location can affect the robot's movement speed, and the system is designed to handle emergency situations accordingly 💼.

## 🛠️ Setup and Working Process:
🖥️ This project is developed using [Docker](https://hub.docker.com/r/carms84/exproblab) which has all the necessary dependencies installed. If you don't want to use Docker and prefer to install the dependencies manually, you'll need to install Armor, SMACH, and since this is a ROS Noetic based project. Once the dependencies are installed, you'll need to clone the following Git link to your workspace and load the OWL file as per the command described in the script, adding the path of the OWL file manually at your convenience.

                                             https://github.com/yeshwanthguru/Experimental-Robotics-1.git


in your workspace and load the owl file as per the command described in the script as your convenience manually adding the path of the owl file . Then do

                                                catkin_make


rocketOnce everything build.To execute the script with simulation do roslaunch command .
                                         
                                         roslaunch expo_assignment_1 survailence_robot.launch

# Results
The following has been attached at initially gave the result without the simulation environment:


### System Limitations
🛑 Our system currently has a few limitations that users should be aware of. The ontology needs to be loaded manually and the possible hypotheses are limited.

### Improvements

🤖🗺️ This assignment is a promising starting point for a ROS-based state machine that enables a robot to navigate a topological map of an environment with ontology. However, several technical improvements can be made to enhance its capabilities, including:

🎛️ Sensor Fusion: By combining data from multiple sensors, such as cameras, lidars, and IMUs, the robot can create a more accurate map of the environment, improving its navigation and decision-making capabilities.

🧠 Machine Learning Integration: Incorporating machine learning algorithms can enable the robot to learn from its experiences and optimize its navigation strategy based on the environment it operates in.

🌐 Multi-Robot Coordination: By coordinating with other robots in the same environment, the robot can avoid collisions and optimize its path planning, ultimately improving overall efficiency.

📈 Online Map Updating: Updating the ontology map in real-time can help the robot adapt to changes in the environment, such as moving obstacles or dynamic objects, making its navigation more accurate and reliable.

🏥 Emergency Response Planning: Enhancing the emergency mode by incorporating more complex planning and response strategies can help the robot respond to emergency situations more efficiently, potentially saving lives. 🚑🚨


### ADITIONAL IMPROVEMENT INSPIRED 

🤖 By leveraging quantum-inspired algorithms, it is possible to implement autonomous navigation and decision-making capabilities in mobile robots, allowing them to operate in complex and dynamic environments with greater efficiency and accuracy. This can open up new possibilities for applications such as 🚨 search and rescue, 🏭 industrial automation, and more. With ongoing research and development in this area, the potential for quantum-inspired robotics is only set to 📈 grow in the future.It has been done with the integration of ros and qiskit.which was inspired from the 
http://www.quantum-robot.org/

where the following task can be executed by the decision making node [Decision-make node] https://github.com/yeshwanthguru/q-robot-Thesis-Introductory/blob/test_main/tiago_testmain2.py

which has the single sensory integration for reference meanwhile the multi sensroy can be done based on the scenario that need to be achieved .
By making these improvements, we aim to provide a more attractive and user-friendly system for our users. Our goal is to help investigators to solve crimes quickly and efficiently, ultimately making our communities safer.

         
![robit-robot](https://user-images.githubusercontent.com/72270080/218888824-9766d4f7-d0f7-46cd-913e-be46becf1da0.gif)[Click me here to see in gazebo environment(Assignment 2)](https://github.com/yeshwanthguru/Experimental-robotics-2.git)
