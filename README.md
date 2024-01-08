# iiithyd
iot platform 
Simulator for Hardware Nodes
This project is a simulator for three different hardware nodes that generate data in the format of the CSV files provided. The simulator can be used to test an IOT platform by sending the generated data to it periodically.

Requirements
Python 3.x
Flask
Pandas
Requests
Installation
Install the required packages using pip:
#bash
pip install Flask pandas requests
Download the CSV files for the three sensors from the provided zip file and place them in the same directory as the simulator code.
Usage
Run the simulator using the following command:
bash
Download
Copy code
python simulator.py
To simulate the data for a specific sensor, send a POST request to the /simulate_node endpoint with the node_type parameter set to the appropriate sensor type. For example, using curl:
bash
Download
Copy code
curl -X POST -F "node_type=AQ" http://localhost:5000/simulate_node
The simulator will generate random data for the specified sensor and send it to the IOT platform. The response status will be displayed in the browser or terminal.
Assumptions
The IOT platform has a REST API endpoint that accepts POST requests with JSON data.
The JSON data format matches the format of the CSV files provided.
The IOT platform can handle the frequency of the POST requests sent by the simulator.
Notes
The simulator generates random data for each sensor within the range of the actual values.
The simulator can be run on any machine with Python 3.x installed.
The simulator can be customized to send data to different IOT platforms by modifying the send_data_to_iot_platform function.
Performance Analysis
To analyze the performance of the platform, you can measure the time it takes for the simulator to generate and send the data to the IOT platform. You can also measure the response time of the IOT platform by measuring the time it takes for the simulator to receive a response after sending the data.

Data Visualization
To visualize the data, you can use any visualization tool or code up the frontend. The data can be fetched live from the platform using the IOT platform's API.
