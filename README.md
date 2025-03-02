<a href="https://npedraza09.github.io">Back to My Portfolio</a>

# Real-Time IoT Data Streaming

This project is designed to enable robust, fault-tolerant data streaming by leveraging Confluent’s Docker image for ZooKeeper, the Kafka broker, and Control Center. Real-time vehicle location data is produced through a Python client and consumed by a Node.js web server, which visualizes IoT streams in a user-friendly interface. By uniting Docker, Python, and Node.js, the system ensures seamless message production, consumption, and fault-tolerant data handling, illustrating a comprehensive, end-to-end approach to real-time data processing.


## Steps to run this project
1. Either fork or download the folder in this repository and open it in your code editor
2. Install all necesssary dependencies
3. In your Terminal, navigate to RealTimeIotDataStreaming/kafka-docker and run `docker-compose up` to create and start the Kafka container
4. Open your browser and navigate to http://localhost:9021. This is the Confluent Control Center, and it will allow you to check the status of the Kafka cluster that you spun up
5. In the Confluent Control Center, navigate to topics, add a topic named "vehicle-coordinates", set the number of partitions to 1, and select "Create with default settings"
6. In a Terminal window, navigate to the "RealTimeIotDataStreaming" folder. Start the web page by running the following command: `node server.js`
7. Navigate to http://localhost:5000. Your web page should be titled “Confluence Kafka REST” and have a button labeled “Consume Vehicle Coordinates”
8. Select the “Consume Vehicle Coordinates” button to verify that your data is being consumed and that there are no errors

## Features
- Simulated stream of real-time vehicle location
- Visualization of IoT streams in a user-friendly interface
- Data consumed in node.js server
  
  ## Future Features
- Live data analysis
- More data visualization and interaction in web app UI

## Tools:
* Python
* JavaScript
* JSON
* Kafka
* Node.js
* Libraries: Kafka

## What the project looks like

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/d7496ab1-0944-4126-8eff-1a0c56d8cd3e" />

<img width="800" height="400" alt="image" src="https://github.com/user-attachments/assets/536c5cce-bc77-4298-9214-1cd70facfc24" />





