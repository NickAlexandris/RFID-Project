# RFID-Project
This project is based on an RF120C RFID reader and a Siemens S7-1214C DC/DC PLC.
The main purpose is to identify users via RFID and start a motor when permission is granted.

Although the concept seems simple, continuous RFID reading caused some unexpected behavior — especially when the antenna was turned off.
After several simulations and tests, I managed to stabilize the logic and bring the project closer to a real-world implementation.

Main Features

User identification via RFID (RF120C)

Access permission logic handled by Siemens S7-1200 PLC

Automatic motor start upon successful identification

Fault and antenna-off handling

Tested in simulation and real setup
