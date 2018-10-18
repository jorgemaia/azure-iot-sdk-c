# Using the Azure IoT C SDK on Ubuntu

This sample shows how to create a program that uses the Azure IoT SDK C package on Ubuntu apt package manager.

## Setting up IoT Hub Environment

1. If you have not already, follow the instructions [here](link!) to set up your IoT Hub enviornment on Azure.

2. Create a IoT Hub device and copy it's device connection string to be used later. Instructions on this can also be found in the link in step 1.
   
3. Make sure you have **CMake**, **g++**, and **gcc** installed on your development machine

    ```Shell
    sudo apt install cmake build-essential
    ```

## Install Azure IoT C SDK on Your Machine

We will use the `apt` package manager to download the binaries needed to build an IoT Hub client application using C.

1. Add the Azure IoT repository

    ```Shell
    sudo apt install -y software-properties-common
    sudo add-apt-repository ppa:aziotsdklinux/ppa-azureiot
    sudo apt update
    ```

2. Install the azure-iot-sdk-c-dev package

    ```Shell
    sudo apt install -y azure-iot-sdk-c-dev
    ```

3. If you haven't already, clone the Azure IoT C SDK repo from Github

    ```Shell
    git clone  https://github.com/Azure/azure-iot-sdk-c.git
    cd azure-iot-sdk-c
    git submodule update --init --recursive
    ```

## Create an Application

We will use `iothub_ll_telemetry_sample` to demonstrate compiling and running a sample.

1. Note the location where you have cloned the `azure-iot-sdk-c` repo. We will assume it is cloned to the home directory for convenience, but if not you can adjust the path accordingly.

   ```Shell
   cd ~/azure-iot-sdk-c/
   ```

2. You now will use the device connection string you copied while setting up the IoT Hub Enviornment. Using your favorite text editor (we will use nano), edit the `iothub_ll_telemetry_sample` file.

    ```Shell
    nano iothub_client/samples/iothub_ll_telemetry_sample/iothub_ll_telemetry_sample.c
    ```

    Find the line containing the following code...

    ```Shell
    static const char* connectionString = "[device connection string]";
    ```

    ...and **update** the string between the quotations with your own device connection string.

    ```Shell
    static const char* connectionString = "HostName=foo;DeviceID=fooDevice;SharedAccessKey=fooKey";
    ```

    Save and close the file.

3. Build the sample using cmake. First navigate to the sample folder.

    ```Shell
    cd ~/azure-iot-sdk-c/iothub_client/samples/iothub_ll_telemetry_sample/linux/
    ```

    Then compile using cmake.

    ```Shell
    cmake .
    ```

    Finally, build the sample.

    ```Shell
    cmake --build .
    ```

## Run the Sample Application

Once the sample application has been built using cmake, you can simply **run it**

```Shell
./iothub_ll_telemetry_sample
```

Did everything work? If so, you should see approximately the following output:

```Shell
Creating IoTHub Device handle
Sending message 1 to IoTHub
Sending message 2 to IoTHub
Sending message 3 to IoTHub
Sending message 4 to IoTHub
Sending message 5 to IoTHub
-> 00:07:23 CONNECT | VER: 4 | KEEPALIVE: 240 | FLAGS: 192 | USERNAME: yosephhub.azure-devices.net/testDevice/?api-version=2017-11-08-preview&DeviceClientType=iothubclient%2f1.2.10%20(native%3b%20Linux%3b%20x86_64) | PWD: XXXX | CLEAN: 0
<- 00:07:23 CONNACK | SESSION_PRESENT: true | RETURN_CODE: 0x0
The device client is connected to iothub
-> 00:07:23 PUBLISH | IS_DUP: false | RETAIN: 0 | QOS: DELIVER_AT_LEAST_ONCE | TOPIC_NAME: devices/testDevice/messages/events/property_key=property_value | PACKET_ID: 2 | PAYLOAD_LEN: 12
-> 00:07:23 PUBLISH | IS_DUP: false | RETAIN: 0 | QOS: DELIVER_AT_LEAST_ONCE | TOPIC_NAME: devices/testDevice/messages/events/property_key=property_value | PACKET_ID: 3 | PAYLOAD_LEN: 12
-> 00:07:23 PUBLISH | IS_DUP: false | RETAIN: 0 | QOS: DELIVER_AT_LEAST_ONCE | TOPIC_NAME: devices/testDevice/messages/events/property_key=property_value | PACKET_ID: 4 | PAYLOAD_LEN: 12
-> 00:07:23 PUBLISH | IS_DUP: false | RETAIN: 0 | QOS: DELIVER_AT_LEAST_ONCE | TOPIC_NAME: devices/testDevice/messages/events/property_key=property_value | PACKET_ID: 5 | PAYLOAD_LEN: 12
-> 00:07:23 PUBLISH | IS_DUP: false | RETAIN: 0 | QOS: DELIVER_AT_LEAST_ONCE | TOPIC_NAME: devices/testDevice/messages/events/property_key=property_value | PACKET_ID: 6 | PAYLOAD_LEN: 12
<- 00:07:24 PUBACK | PACKET_ID: 2
Confirmation callback received for message 1 with result IOTHUB_CLIENT_CONFIRMATION_OK
<- 00:07:24 PUBACK | PACKET_ID: 3
Confirmation callback received for message 2 with result IOTHUB_CLIENT_CONFIRMATION_OK
<- 00:07:24 PUBACK | PACKET_ID: 4
Confirmation callback received for message 3 with result IOTHUB_CLIENT_CONFIRMATION_OK
<- 00:07:24 PUBACK | PACKET_ID: 5
Confirmation callback received for message 4 with result IOTHUB_CLIENT_CONFIRMATION_OK
<- 00:07:24 PUBACK | PACKET_ID: 6
Confirmation callback received for message 5 with result IOTHUB_CLIENT_CONFIRMATION_OK
-> 00:07:24 DISCONNECT
Press any key to continue
```

That's it. You've compiled and run a sample using the low level (\_ll\_) C SDK. For more samples explore the samples folder [**here**](./iothub_client/samples/).