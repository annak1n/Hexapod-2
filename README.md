# Hexapod

![Hexapod](/Doc/hexapod_meca.png?raw=true "Hexapod")

The Hexapod is a 6 legs bug made from 18 servos, a Pololu Maestro and a Raspberry PI3

This Hexapod is controlled by an Android device over a Wifi using TCP protocol.
## Authors
* **Aurelien Burdot** - *Continuous devlopment* -
* **Kevin Leveque** - *Arduino Kinetic* -

## Video
![Video of the Hexapod walking](https://youtu.be/1qGUNXRVS8o)

## Set up
### Wiring
![Wiring](/Doc/Wire_setup.jpg?raw=true "Wiring")

### Pololu
Use the TX/RX pin of the Raspberry
Connect the USB port of the Pololu to the Raspberry (for power)

### Serial Config
In the main.c change the port and the baudrate
```
int fd = SerialConfig("/dev/serial0", 9600);
```

Default serial port for RX/TX pin
```
/dev/serial0
```

## Compile

```
make
```

## Start the program

```
./Hexapod
```
## Add program to start-up app list

Add the path of the binary in the file:
```
/etc/rc.local
```
## Remote Android App

![GitHub Android App](https://github.com/AurelienBu/WowWeeRemote)

## Commande to send over TCP protocol

### Go forward
```
fd+
```

### Stop and get up
```
s++
```

### Sit down
```
bd+
```

### Turn left
```
l+
```

### Turn Right
```
r+
```
