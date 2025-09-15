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
- SQL Table queries (under sql_queries.sql)
- Trigger Function queries (under sql_queries.sql)

For testing:
- client.py (refer Files)

------------------------------------------------------------

How to Setup AquaSense Server?

[INSTRUCTIONS]
1.) Install the following:
    - Python
    - PostgreSQL
        Credentials:
        - host     = localhost
        - dbname   = postgres
        - user     = postgres
        - password = 1234
        - port     = 5432
    - TimescaleDB

2.) Open pgAdmin 
    - Locate the following inside the project folder:
        - sql_queries.sql
        - ./setup 
    - Using "sql_queries.sql", query all command (create tables, create trigger functions, additional queries)
    - Under "./setup" folder, import all .csv files to its corresponding table (Import in pgAdmin) 

3.) Setup files (.env, credentials.json)
    - Locate the following files inside the project folder:
        - .env
        - credentials.json
    - cd to "C:\Users\Public"
    - Place .env and credentials.json

4.) Run "AquaSense-Server.exe"
    - If run successfully, the server will ask for your IP and port (OS to be added soon)
    - Upon inputting the IP and port, the server will automatically synchronize the Firebase configuration data to the local configuration
    - Once configured, the server will be actively looking for connection, ready to be deployed.


--------------------------------------

[TESTING]
1.) Locate client.py
2.) Setup the socket connection such that it matches the server.
3.) If socket connection is successfully made, "client.py" will continuously send a random data to the server (per second)
