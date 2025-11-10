RFID Access Control Project
 Overview

//This project implements an RFID-based access control system using a Siemens S7-1214C DC/DC PLC and an RF120C RFID reader.
//The primary objective is to identify users via RFID and automatically start a motor when valid access permission is granted.

 Main Features
-RFID-based user identification using the Siemens RF120C module
-Access permission control managed directly by the S7-1214C PLC
-Automatic motor activation upon successful user authentication
-Robust logic ensuring stable performance during antenna ON/OFF transitions
-Validated through both simulation and physical testing

Implementation Notes

//When working with RFID transponders, it is crucial to check the available memory space on your specific card.
//For example, the MDS D100 offers only 112 bytes of memory, so you must consider the data length used in your UDTs or Data Blocks (DBs).
//Always refer to the documentation of your specific transponder type to ensure compatibility and reliable operation.

References & Documentation

Transponder Addressing Guide:https://support.industry.siemens.com/cs/mdm/109781633?c=132222750091&dl=es&lc=cs-CZ

Siemens Support Article: https://cache.industry.siemens.com/dl/files/939/96784939/att_931671/v1/96784939_S7-1200_RF120C_Set13_DOC_v2d0_en.pdf

Summary

This RFID project demonstrates a practical and scalable access control solution integrated directly into a Siemens PLC system.
The design emphasizes stability, modular programming, and real-world reliability, serving as a solid foundation for more advanced industrial automation applications.

All control logic is written in Structured Control Language (SCL) for enhanced readability and modularity.
