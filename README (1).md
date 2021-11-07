# Connecting to Android using ADB

## Connecting to Android using ADB

Android Debug Bridge (ADB)

* USB debugging on the device must be enabled
* Devices are connected to the same network
* Device is listening on TCP/IP port 5555
* ​

1. Set device to listen to 5555
2. Connect to the device by its IP
3. Confirm connection

```
$ adb tcpip 5555
$ adb connect x.x.x.x:5555
$ adb devices
```

​
