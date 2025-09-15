============================================================================================
                            AQUASENSE SERVER SETUP GUIDE
============================================================================================

[MAIN]
AQUASENSE SERVER

[OVERVIEW]
AquaSense Server is the backend for near real-time monitoring of aquaculture environments. It captures sensor data from the Things Layer, preprocess the raw data, log the processed data to the PostgreSQLTimescaleDB and Firebase for seamless storage and visualization in the frontend (AquaSense).

[FEATURES]
- Near Real-time data collection from IoT devices.
- Connectivity checks between IoT Layers.
- Multi-threaded server for concurrent/parallel server processing and operation.
- Database redundancy - storage for Firebase RTDB and TimescaleDB (PostgreSQL extension).
- Firebase integration for data visualization.
- Notification system for near real-time remote alerts.
- Remote configuration of ports (Things Layer).
- Duplex communication of actuation data from the different layers.
- Formula data for configurable and calibratable ports.
- Server data

[MIN_SYSTEM_REQUIREMENTS]
- OS: Windows 10 (Linux to be tested)
- Architecture: 64-bit (x86_64) system
- Python 3
- PostgreSQL 16+ (with TimescaleDB extension)


[PREREQUISITE]
Files Needed:
- AquaSense-Server.exe
- .env (for DB credentials)
- credentials.json (for Firebase RTDB init)

Initial Deployment:
- Database initial data (saved in .csv)
- SQL Table queries
- Trigger Function queries

For testing:
- client.py (refer Files)

------------------------------------------------------------

[INSTRUCTIONS]
1.) 