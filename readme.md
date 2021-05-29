# Entfernungsmessung (Time of Flight) Proof of Concept

## Aufbau

- Visual Studio Code mit Plattform IO
- Programer AVRISP mkII
- Arduino Uno ohne Bootloader
- Breakout Platine VL53L0X Time-of-Flight (ToF) Laser Abstandssensor von AliEx
-  Code Adafruit_VL53L0X-Bibliothek und daraus Beispiel *vl53l0x*
- Verschaltung
  - Versorgungsspannung 5V und GND
  - Datenverbindung SDA,SCL
  - XSHUT, GPIO nicht verwendet pullups auf breakoutboard



![img](.\misc\adafruit_products_VL53L0X.png)



## Funktion

- Beispielcode 1:1 aus Bibliothek kopiert und mit AVRISO mkII Programer (libusbK USB Driver) geladen.
- Platformio.ini angepasst für Programer und serielle Schnittstelle
- Nach der Programmierung kann der Sensor nicht gebootet werden. Nach Reset funktioniert die Abstandsmessung dann.
- Ausgabe der Messwerte permanent auf der seriellen Schnittstelle
- Bereich bis ca. 45cm für Hand und bis ca 110cm für ein Blatt Papier
- Range-Umstellung nicht getestet