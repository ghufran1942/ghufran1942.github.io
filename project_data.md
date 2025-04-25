Detailed Project Summary

Heterogeneous Robot Coordination

Motivation

The primary goal of this project was to develop a robust system for coordinating heterogeneous robots, including drones and quadrupeds, to perform tasks such as formation control, obstacle avoidance, and synchronized movement. The project aimed to explore the integration of advanced technologies like ROS2, SLAM, GPS, and Vicon systems to enable seamless collaboration between different robotic platforms.

What Was Done

- Installed ROS2 on Raspberry Pi 4B and Raspberry Pi 2W via docker.

- Integrated Vicon systems, and ZED cameras for precise positioning and navigation.

- Developed ROS packages to control the agents, object detection, and path planning.

- Conducted over 130 tests, including formation control and obstacle avoidance.

- Used ROS-Bridge for seamless communication between ROS1 and ROS2.

What Was Learned

- Synchronization between heterogeneous robots is critical for effective coordination.

- Communication reliability is a significant challenge in multi-robot systems, especially in bandwidth-constrained environments.

- Object detection models must adapt to varying lighting conditions and environments for consistent performance.

    - Just Camera is not enough in outdoor conditions. Camera needs to be complemented with LIDAR or other sensor for autonomous navigation.

What Was Achieved

- Successfully demonstrated drone and quadruped coordination using Vicon and GPS systems.

- Developed a robust ROS2 package for object detection and avoidence, and path planning.

- Published results in academic papers and contributed to the development of new methodologies for heterogeneous robot coordination.

Image Placeholders

Image 1: System setup with drones and quadrupeds (refer to page 10 of WPR.pdf).

Image 2: Test results of formation control (refer to page 12 of WPR.pdf).

Image 3: SLAM implementation and mapping (refer to page 15 of WPR.pdf).

Deformable Project - Aerial and Ground

Motivation

This project focused on the development of deformable robots, both aerial and ground-based, to adapt to dynamic environments. The primary objective was to design to reduce the weight for aerial agents and improve integration of the ground robots.

What Was Done

- Integrated microROS on Xiao ESP32C3 chipsets for ground robots.

- Designed and tested control systems for servo motors.

- Conducted extensive tests on ground robots to evaluate deformation control.

- Iterated designs for motor mounts and frames to improve stability and performance.

What Was Learned

- Integrating microROS with various hardware components presents unique challenges.

- Iterative design is essential for achieving optimal performance in deformable robots.

- Effective teaching and mentoring methods are critical for successful collaboration in robotics projects.

What Was Achieved

- Successfully demostrated takeoff aerial robots and control of ground robots.

- Developed a robust system for servo motor control using ROS2.

- Contributed to the development of new methodologies for deformable robot control.

Image Placeholders

Image 1: Ground robot setup with microROS (refer to page 18 of WPR.pdf).

Image 2: Test results of deformation control (refer to page 20 of WPR.pdf).

Image 3: Iterated designs for motor mounts and frames (refer to page 22 of WPR.pdf).

VR - Hexacopter

Motivation

The VR-Hexacopter project aimed to integrate virtual reality (VR) technology with hexacopters to enhance remote operation and 3D spatial awareness. The project explored the use of ZED cameras and Jetson modules for real-time video streaming, object detection, and data visualization.

What Was Done

- Designed and printed mounts for ZED cameras and Jetson modules on hexacopters.

- Iterated designs for camera mounts to improve stability and performance.

What Was Learned

- Integrating VR systems with aerial robots requires careful consideration of hardware and software compatibility.

What Was Achieved

- Successfully integrated the hardware components of the hexacopter to enable development on 3D point cloud points and creation of maps in VR.

- Developed a robust system for real-time video streaming and object detection.

- Contributed to academic research and publications in the field of VR and robotics.

Image Placeholders

Image 1: Hexacopter setup with ZED camera and Jetson module (refer to page 25 of WPR.pdf).

Image 2: Test results of VR-controlled flights (refer to page 27 of WPR.pdf).

Image 3: Iterated designs for camera mounts (refer to page 30 of WPR.pdf).

### Project Name: Development of Sanitization Drone

#### Motivation
- The COVID-19 pandemic has significantly impacted health, economy, and daily life globally.
- Sanitizing large areas like halls, malls, parks, and streets is challenging, requiring significant manpower and time.
- Manual sanitization methods (e.g., hand pumps) are slow and tedious.
- Prolonged exposure to sanitizers can cause health risks such as skin irritation, respiratory issues, and liver damage.
- Drones offer an effective solution for large-scale sanitization, reducing human effort and exposure.

#### What was Done
- Designed and developed a 3D-printed quadcopter equipped with a sanitizer reservoir and spray system.
- Conducted thrust calculations and selected components such as motors, batteries, and flight controllers.
- Iterated the design to improve weight, strength, and aesthetics:
  - Scaled down from a full-size agricultural drone to a 265 mm frame.
  - Replaced plates with grills for lightweighting.
  - Improved motor mounts for better fit.
- Conducted stress analysis and motion studies to ensure structural integrity and performance.
- Selected Polylactic Acid (PLA) as the primary material for 3D printing based on strength, printability, and cost.
- Created a bill of materials and initiated procurement of components.

#### What was Learned
- The importance of material selection in drone design, balancing strength, weight, and cost.
- The iterative design process to optimize performance and resource utilization.
- Practical challenges in integrating components like motors, batteries, and spray systems.
- The role of simulations (e.g., stress analysis) in validating design decisions.

#### What was Achieved
- Developed a functional drone design with the following specifications:
  - Estimated Flight time: ~8.2 minutes (at 80% battery discharge).
  - Weight: 1.7 kg (below the 2 kg target).
  - Estimated Thrust-to-weight ratio: ~4:1 (exceeding the 3:1 target).
- Designed a 660 ml sanitizer container with an aerodynamic shape and assembly mounts.

### Ultrasound Guidance via Q-Learning

#### Motivation
- The project was inspired by the idea of enabling a robot to learn how to guide a human to a goal in the fastest and most efficient way possible.
- It addresses challenges in scenarios where users need to use personal medical equipment, ensuring that the robot can guide the user to attach the equipment in the correct position.

#### What Was Done
- **Project Description**:
  - Developed a one-dimensional ultrasound guidance system using Q-learning.
  - Connected Q-tables (randomized and simulated) to a track system to guide a user-controlled device to a target location.
  - Used two motors for directional guidance: left motor for leftward movement, right motor for rightward movement, and no motor activation for staying in place.
  - Incorporated a reward system to improve Q-table guidance over time.

- **Physical Setup**:
  - Built a movable device with a breadboard, PIC microcontroller, motor driver, ultrasound sensor, and RS232 connector.
  - Device operates on a track with a range of 5-28 inches, corresponding to 23 states in the Q-table.

- **Electrical Components**:
  - **Sensors**:
    - Ultrasound Sensor (HC-SR04) for position detection.
    - Specifications: 5V DC, 15mA, 15° angle, 2cm-4m range.
  - **Actuators**:
    - Motors controlled via pulse-width modulation (PWM) signals.
    - Motor driver (L293B) to apply PWM signals to the motors.

- **Q-Learning Implementation**:
  - Initialized a random Q-table with states as rows and actions as columns.
  - Used an epsilon value of 1 to prioritize exploitation over exploration.
  - Updated Q-values using the Bellman equation:
    \[
    Q(s_t, a_t) = Q(s_t, a_t) + \alpha \cdot [R_{t+1} + \gamma \cdot \max_a Q(s_{t+1}, a) - Q(s_t, a_t)]
    \]
  - Trained the system over 50 episodes, visualizing the Q-table evolution using MATLAB.

- **Program Flow**:
  - Initialized Q-table.
  - Read ultrasonic sensor data.
  - Selected an action based on the Q-table.
  - Performed the action and measured the reward.
  - Updated the Q-table based on the reward and state transition.

#### What Was Learned
- The robot successfully learned to guide the user to the goal efficiently by improving its decision-making over time.
- The Q-learning algorithm demonstrated its ability to adapt and refine the guidance system through repeated training episodes.
- The system highlighted the potential of reinforcement learning in real-world applications, particularly in scenarios requiring precise guidance.

#### What Was Achieved
- Successfully implemented a Q-learning-based guidance system for a 1D track.
- Demonstrated the evolution of the Q-table over 20 episodes, showing improved decision-making.
- Highlighted the potential for using reinforcement learning in real-world applications like medical equipment guidance and motion assistance systems.

### Smart Integrated Mobility Solutions

#### Motivation
- To find the most optimal route for traveling from point A to point B by utilizing various modes of transportation, optimizing for both time and cost.

#### What Was Done
- **Setup and Libraries**:
  - Installed required libraries (`networkx`, `googlemaps`, `matplotlib`) for graph-based modeling and API integration.
  - Configured APIs for Google Maps and Booking.com (expired keys were used in the document).

- **User Input Widgets**:
  - Created interactive widgets for:
    - Selecting trip type (One Way or Round Trip).
    - Inputting departure and destination locations.
    - Choosing departure and return dates.
    - Selecting transportation modes (transit, driving, walking).
    - Filtering results by Cheapest, Fastest, or Most Comfortable options.

- **Data Retrieval**:
  - Used Google Maps API to:
    - Fetch directions, distances, and travel times for various modes of transport.
    - Identify nearby international airports based on geolocation.
  - Integrated Booking.com API to:
    - Fetch flight details, including prices, departure/arrival times, and layovers.

- **Cost and Time Calculations**:
  - Developed a cost calculator for different transportation modes (driving, transit, etc.).
  - Calculated travel costs and times for each segment of the journey.

- **Graph Construction**:
  - Built a directed graph using `networkx` to represent travel routes and connections.
  - Nodes represent locations (e.g., origin, destination, airports).
  - Edges represent travel options with attributes like mode, cost, and time.

- **Pathfinding**:
  - Implemented the A* algorithm to find the optimal path between the origin and destination based on cost and time.
  - Visualized the graph and highlighted the A* path.

#### What Was Learned
Here’s the "What Was Learned" section condensed into **4 strong bullet points**:

---

### What Was Learned
Got it — you want a **main bullet → sub-bullet** style structure, which looks clean and professional for a portfolio.

Here’s the "What Was Learned" section rewritten like that:

---

### What Was Learned
  - **API Integration**
    - Handled authentication, rate limits, and incomplete data responses from Google Maps and Booking.com.
    
  - **Graph Modeling**
    - Built a directed graph to represent multi-modal travel routes with cost and time as weighted edges.
    - Balanced real-world transportation complexity with efficient, scalable graph abstraction.

  - **Pathfinding Optimization**
    - Implemented the A* algorithm with careful heuristic design for realistic and efficient route finding.
    - Learned how different heuristics impact search performance and travel plan quality.

  - **System Architecture and Robustness**
    - Designed modular, scalable code to connect user input, API data, graph construction, and optimization logic.
    - Built error handling and validation layers to gracefully manage dynamic and unpredictable real-world data.

#### What Was Achieved
- Successfully created an interactive system for planning multi-modal travel routes.
- Integrated APIs to fetch real-time data for transportation and flights.
- Built a graph-based model to represent and analyze travel options.
- Implemented A* pathfinding to determine the most efficient travel route.
- Visualized the travel graph and optimal path for better understanding.


### STEM Curriculum Recommender

#### Motivation
- The goal of this project is to streamline the process of matching educational content to specific topics in a curriculum. 
- The aim is to develop an accurate and efficient model trained on a library of K-12 educational materials organized into various topic taxonomies.
- These materials are in diverse languages and cover a wide range of topics, particularly in STEM (Science, Technology, Engineering, and Mathematics).
- The ultimate objective is to enable students and educators to more readily access relevant educational content to support and supplement learning.

#### What Was Done
- **Data Loading and Preprocessing**:
  - Loaded datasets: `content.csv`, `correlations.csv`, and `topics.csv`.
  - Filtered datasets to include only English-language content and topics.
  - Focused on content available as documents, videos, or HTML5 formats.
  - Dropped rows with missing values.

- **Data Filtering**:
  - Filtered topics and content based on their presence in the correlations dataset.
  - Exploded the correlations dataset to associate each topic with multiple content items.
  - Counted the number of content items available for each topic and identified the top three topics with the most content.

- **Text Preprocessing**:
  - Removed stopwords, links, special characters, and numbers from the text.
  - Converted text to lowercase and removed excessive whitespace.
  - Created a combined "corpus" column by merging the title, description, and text fields.

- **TF-IDF Vectorization**:
  - Applied TF-IDF (Term Frequency-Inverse Document Frequency) to the cleaned text data to create feature vectors.

- **Clustering**:
  - Used KMeans clustering with 2 clusters to group the content.
  - Reduced the dimensionality of the feature vectors using PCA (Principal Component Analysis) for visualization.

- **Keyword Extraction**:
  - Extracted the top 10 keywords for each cluster using the TF-IDF vectors.

- **Cluster Mapping**:
  - Mapped clusters to labels (e.g., "Topic 1" and "Topic 2").

- **Visualization**:
  - Created a scatter plot to visualize the clusters using the PCA-reduced dimensions.

#### What Was Learned
- **Effectiveness of Clustering**:
  - The clustering was highly effective, achieving a 95% match for similar content.
  
- **Challenges Faced**:
  - Preprocessing challenges included handling missing values and ensuring the removal of irrelevant text elements like links and special characters.
  - Clustering challenges involved determining the optimal number of clusters and ensuring meaningful separation between clusters.

#### What Was Achieved
- Successfully filtered and preprocessed a large dataset of STEM-related content.
- Identified clusters of content based on textual similarity using TF-IDF and KMeans.
- Extracted meaningful keywords for each cluster to understand the themes.
- Visualized the clusters in a 2D space using PCA.
- Created a new curriculum dataframe with clustered content, ready for recommendations.
- Enabled a streamlined process for matching educational content to specific topics, improving accessibility for students and educators.
