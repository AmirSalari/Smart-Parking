# Smart-Parking
An IoT Based Smart Parking System Using LoRa

# Overview

The LoRaWAN smart-parking solution used an Arduino based sensor node, a single-tech LoRa Gateway, TTN to host the Parking application server. The following are the detailed steps of how the application works:

1- The Arduino board detects the status of the parking spot by using an HC-SR04 ultrasonic sensors.

2- The status data is sent to the Single-Tech LoRa gateway via a RF95 Transceiver LoRa module connected to the Arduino board via serial connection.

3- The LoRa gateway is connected to a LoRa server on thethingsnetwork.org and forwards all packets it receives there

4- The TTN server forwards the received packages to a channel that the Application server is listening on

5- The Application Server also hosted on TTN listens to the PubNub channel and detects the status data of each parking spot.

6- After comparing the parking spot status data with the stored value, the parking application makes the decision of whether or not to send a notice message to the mobile app to update the status of a parking spot