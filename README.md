# Design and Development of an Embedded System for Remote-Controlled Cars
This project involves the modernization of a traditional remote-controlled car by replacing its original communication system with a more modern approach using Bluetooth Low Energy (BLE). The system utilizes an Arduino Nano 33 BLE Sense to control the car’s steering and throttle, and a Flutter application acts as the interface for users to remotely control the car via their smartphones.
## Quick Start
### Prerequisites
To get started, ensure you have the following:
- *Arduino Nano 33 BLE Sense* [Arduino](https://docs.arduino.cc/hardware/nano-33-ble-sense/)
- *RC car* [car](https://traxxas.com/products/models/electric/58034-8-slash) with
  - Servo Motor (for steering control)
  - Electronic Speed Controller (ESC) (for speed and direction control)
- *Smartphone* (with Bluetooth capabilities)
- *Flutter SDK* (to run the mobile application) [Flutter](https://docs.flutter.dev/get-started/install)
- *Arduino IDE* (for programming the Arduino Nano) [Arduino IDE](https://www.arduino.cc/en/software)

  ![RC car](images/figure1.png?raw=true "RC car")
  
  ![Arduino Nano](images/figure_2.png?raw=true "Arduino Nano")
### Hardware Setup
1) Connect the Hardware: Ensure proper wiring between the Arduino Nano 33 BLE Sense, servo motor, and ESC.
  - *Pin 9*: Connected to the servo motor for steering.
  - *Pin 10*: Connected to the ESC for throttle control.
  - *Ground* (GND): Shared ground connection for all components.
2) Powering the Arduino: You can either power the Arduino via its onboard battery or via USB when uploading the code.

![Components](images/figure_4.png?raw=true "Components")
![Connections](images/figure_5.png?raw=true "Connections")

### Arduino Setup
1) Download and install the Arduino IDE.
2) Clone or download this repository.
3) Open the Arduino sketch main.ino located in the edge/ folder.
4) Connect your Arduino Nano 33 BLE Sense via USB to your computer.
5) Select the correct Board and Port in the Arduino IDE (Arduino Nano 33 BLE).
6) Install the necessary libraries for Arduino:
	- Servo.h [download link](https://docs.arduino.cc/libraries/servo/)
	- ArduinoBLE.h [download link](https://docs.arduino.cc/libraries/arduinoble/)
7) Upload the code to the Arduino Nano.
### Flutter App Setup
1) Install Flutter.
2) Navigate to the client/ folder of the project.
3) Open the project in your preferred IDE (Android Studio or VS Code).
4) Connect your smartphone via USB (ensure Developer Mode is enabled).
5) Run the Flutter app on your device using the following command:
flutter run
6) The app will be installed and launched on your smartphone.
### Controlling the Car via BLE
1) Power on the Arduino Nano and open the Flutter app.
2) Scan for nearby BLE devices and connect to the car's module (named Measurify-Car).
3) Use the joystick in the app to control steering and throttle.

![Smartphone app](images/figure_3.png?raw=true "Smartphone app")
