# Overview - Azure IoT C SDK

The Azure IoT C SDK and accompanying libraries enable developers to more easily create IoT solutions written in C for Azure and the Azure IoT platform.

[![Build Status](https://azure-iot-sdks.visualstudio.com/azure-iot-sdks/_apis/build/status/c/integrate-into-repo-c)](https://azure-iot-sdks.visualstudio.com/azure-iot-sdks/_build/latest?definitionId=14)

# Getting Started

### New to Azure IoT Hub?

* **Introduction to Azure IoT Hub:** If you have never used the Azure IoT Hub, follow this guide to learn how to set up an IoT Hub and IoT Hub devices. [Linked here.](https://github.com/Azure/azure-iot-device-ecosystem/blob/master/setup_iothub.md) 

### Introducing you to the Azure IoT C SDK.

* **Ubuntu Telemetry Walkthrough:** Explore the Azure IoT C SDK by compiling a sample application that sends telemetry to your IoT Hub device. 
[Linked here.](https://github.com/Azure/azure-iot-sdk-c/blob/master/doc/ubuntu_telemetry_walkthrough.md)

# Components 

* **Azure IoT Hub Device C SDK:** Connect devices running C code to Azure IoT Hub.
* **Azure IoT Hub Service C SDK:** Interface with an Azure IoT Hub service instance from a server-side C application.
* **Azure IoT Hub Provisioning Client SDK:** TODO provisioning_client folder vs provisioning_service_client folder???
* **Azure IoT Hub Device Provisioning Service Client SDK:** Enroll devices with [Azure IoT Device Provisioning Services](https://docs.microsoft.com/azure/iot-dps/) and managing enrollments lists.
* **Serializer Library for C:** A tool to help serialize and deserialize data on your device.


# Packages and Libraries
* **Linux:** [Device SDK on apt-get](./iothub_client/readme.md#aptgetpackage)
* **mbed:**                                      [Device SDK library on MBED](./iothub_client/readme.md#mbed)
* **Arduino:**                                   [Device SDK library in the Arduino IDE](./iothub_client/readme.md#arduino)
* **Windows:**                                   [Device SDK on NuGet](./iothub_client/readme.md#nugetpackage)
* **iOS:**                                       [Device SDK on CocoaPod](https://cocoapods.org/pods/AzureIoTHubClient)

# Samples

* [**Device SDK Samples**](./iothub_client/samples/)
* [**Service SDK Samples**](./iothub_service_client/samples/)
* [**Serializer Library Samples**](./serializer/samples/)

# Compile the SDK

When no package or library is available for your platform or if you want to modify the SDK code, or port the SDK to a new platform, then you can leverage the build environment provided in the repository.
  * [**Compile the Device SDK**](./iothub_client/readme.md#compile)
  * [**Compile the Service SDK**](./iothub_service_client/readme.md#compile)

# SDK API Reference Documentation

The API reference documentation for the C SDKs can be found [here][c-api-reference].

# Other Azure IoT SDKs

To find Azure IoT SDKs in other languages, please refer to the [azure-iot-sdks](https://github.com/azure/azure-iot-sdks) repository.

# Developing Azure IoT Applications

To learn more about building Azure IoT Applications, you can visit the [Azure IoT Dev Center](https://azure.microsoft.com/en-us/develop/iot/).
