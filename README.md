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

FC_SCENARIO is not a standalone block — it’s part of a Siemens demo architecture for RFID communication.
It uses a data block (DB_Interface) to exchange parameters such as:

addrTagRead, lenDataRead

addrTagWrite, lenDataWrite

command/status words, and so on.

However, it only becomes functional once:

The RF120C communication channel is initialized (through FC_WRITE_READ or another comms FC).

The DB_Interface is properly structured with correct default values.

The tag is correctly powered and detected by the antenna.

Without that setup, the RFID reader doesn’t respond to commands → the FC won’t execute properly.D

Main Cycle (OB1)
   |
   --> )FC_WRITE_READ (handles the actual RFID read/write operation)
         |
         --> FC_SCENARIO (handles scenario logic)

