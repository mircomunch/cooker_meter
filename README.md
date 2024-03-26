Cooker Energy Meter
======

An energy meter for cooking experiments analysis

### About

The system is composed by:
- TECKIN smart socket equipped with Wi-Fi
- micro-computer Raspberry Pi (RPi) equipped with a NODE-Red service
- PC that can connect to the RPi through the web dashboard

The RPi ask for data to the socket trough WiFi (voltage, current, power) using propietary API.
Those data are stored in a local database using SQLite and then provided at the user with a web dashboard.
Trought the dashboard the tests can be managed.

### How to connect
- Supply the RPi
- Connect to the WiFi
  - SSID: GREATER
  - PSW: cooker123
- Open the web dashboard at greater.local:1880/ui
- Login
  - user
  - GREATERcooker
- Plug the load trough the socket

### How to use dashboard
- Manage test
  - Insert new test (Unique ID, name and description)
  - Run a test and check the running info selecting the acquisition period (1s - 120s)
  - Delete a test
  - See all tests' status
- Setting
  - Check system status (Socket connection state, last seen, RPi CPU temperature)
  - Get and set current date and time
  - Download Database / Delete Database / Reboot system / Download Log
  - See raw data (test and readings)
  
### How to run a test
1) Insert a new test with the unique ID
2) Select the test in the "Start / Stop" section
3) Start the test ... Stop the test
4) Download the database with all the tests after a certain time
5) Clear the system deleting the database and rebooting the RPi

### How to elaborate data
1) Run node-red and select the directory in wich the db is and the one in wich the tests will be saved
2) Start the program, a .csv file will be created for each test_id containing timestamp, date (HH:mm:ss GG:MM:AAAA), current, voltage, power
3) Into the web dashboard (localhost:1880) there will be the table of AVG and MAX values for each test and a chart with plotted current, voltage and power for each test
