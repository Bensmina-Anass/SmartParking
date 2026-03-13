# Smart Parking Digital Twin

A data engineering and machine learning project for modeling, streaming, storing, and predicting parking occupancy from real sensor data. The system uses **Apache Kafka** for event streaming, **TimescaleDB** for time-series storage, and a **3D parking model** for visualization using **Blender**.

## Dataset

Source: **City of Melbourne — On-street Car Parking Sensor Data (Jan–May 2020)**  
https://data.melbourne.vic.gov.au/explore/dataset/on-street-car-parking-sensor-data-2020-jan-may/information/

The dataset includes parking sensor events such as:

- Arrival time
- Departure time
- Duration
- Parking bay ID
- Parking restrictions
- Vehicle presence

These records make it possible to reconstruct parking occupancy over time and build prediction models.

## Architecture

```text
Dataset -> Kafka Producer -> Kafka Topic -> TimescaleDB -> ML Service -> 3D Visualization
