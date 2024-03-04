cooker
======

an energy meter for cooking expirements analysis

### About

The system is composed by a TECKIN smart socket and a RPi equipped with a NODE-Red service.

The RPi ask for data to the socket trough WiFi (voltage, current, power) using propietary API.
Those data are stored in a local database using SQLite and then provided at the user with a web dashboard.
Trought the dashboard the tests can be managed (inserted/deleted).
Each test is relater to the correspondig power and time used

### How to connect
- Supply the system
- Connect to the WiFi
  - SSID: GREATER
  - PSW: cooker123
- Open the web dashboard at greater.local:1880
- Login
  - user
  - GREATERcooker
- Plug the load

### How to use dashboard
- Manage
  - Insert new test
  - Run a test
  - See all tests' status
- Setting
  - Check socket status
  - Download Database
  - Delete test
  - See raw data (test and readings)  
