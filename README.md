# Real-Time IoT Data Streaming

A Kafka pipeline that streams simulated vehicle GPS coordinates from a Python producer to a Node.js consumer. Built for my MIT Professional Certificate in Data Engineering (2024–2025).

## How it works

1. **Kafka cluster:** Confluent's Docker images run ZooKeeper, the Kafka broker and Control Center (`RealTimeIotDataStreaming/kafka-docker/`).
2. **Producer:** `pythonProducer/PublishVehicleCoordinates.py` creates the `vehicle-coordinates` topic if needed and publishes a random longitude and latitude every 3 seconds.
3. **Consumer:** an Express server (`NodeJSConsumer/server.js`) serves a page with a button that reads the topic using node-rdkafka (`myconsumer.js`, adapted from Confluent's example).

**Built with:** Apache Kafka (Confluent), Docker, Python (kafka-python), Node.js, Express, node-rdkafka

## Run it locally

You need Docker, Python 3 and Node.js.

1. From `RealTimeIotDataStreaming/kafka-docker/`, run `docker-compose up`.
2. Open Confluent Control Center at http://localhost:9021 and create a topic named `vehicle-coordinates` with 1 partition.
3. Start the producer: `pip install kafka-python`, then `python pythonProducer/PublishVehicleCoordinates.py`.
4. From `RealTimeIotDataStreaming/NodeJSConsumer/`, run `npm install`, then `node server.js`.
5. Open http://localhost:5000 and click **Consume Vehicle Coordinates**.

## Screenshots

<img width="800" height="400" alt="Real-Time IoT Data Streaming screenshot" src="https://github.com/user-attachments/assets/d7496ab1-0944-4126-8eff-1a0c56d8cd3e" />

<img width="800" height="400" alt="Real-Time IoT Data Streaming screenshot" src="https://github.com/user-attachments/assets/536c5cce-bc77-4298-9214-1cd70facfc24" />
