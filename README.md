# Arduino-Wifi-boiler-thermostat
Tested, Super stable Arduino thermostat board, with Wifi board.
I wanted to build something like an industrilal system with arduinos. 
This project has to boards. One is R3 UNO, other is R4 UNO WIFI.
The R3 controls the boiler relay, and checks flow/ return/ room temperatures. 
Watchdog running on the R3 so if the code is frozen, then it restartes itself.
R4 wifi runs heartbeat signal. If R4 is frozen then R3 restarts it.
R4 also emits "CloudOK" signal. (for example cloud is unreachable, or wifi is off, or just R4 is dropped off from Wifi). If this signal is false for certain time, then R3 restarts it.
The setpoint is arrives from the Cloud, and uploads to the R3. If nothing arrives then R3 runs from the latest setpoint. If no wifi and the power just came back, the default settemp is 14°C.
If R3 founds error  (for example bad sensor, or no heating) if forwards the error towards the R4 which uploads it to the cloud.


You can download the code and the circuit diagram too.
The circuit diagram contains a tested blackout circuit too. (if the VIN voltage is too low then it pulls down the Reset pin of the R3).
PLS  give me some feedback see how it works in the huge world. :)
Sincerely: Zoltán.
