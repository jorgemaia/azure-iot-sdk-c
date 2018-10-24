# Overview - Azure IoT C SDK

<<<<<<< HEAD
The Azure IoT C SDK and accompanying libraries enable developers to more easily create IoT solutions written in C for Azure and the Azure IoT platform.
=======
[![Build Status](https://azure-iot-sdks.visualstudio.com/azure-iot-sdks/_apis/build/status/c/integrate-into-repo-C)](https://azure-iot-sdks.visualstudio.com/azure-iot-sdks/_build/latest?definitionId=85)
>>>>>>> 506cf3e6cdc0f55510aa027cba295aa910cdd341

[![Build Status](https://azure-iot-sdks.visualstudio.com/azure-iot-sdks/_apis/build/status/c/integrate-into-repo-C)](https://azure-iot-sdks.visualstudio.com/azure-iot-sdks/_build/latest?definitionId=85)

# Getting Started

### New to Azure IoT Hub?

* **[Introduction to Azure IoT Hub](https://github.com/Azure/azure-iot-device-ecosystem/blob/master/setup_iothub.md):** Follow this guide to learn how to set up an IoT Hub and IoT Hub devices.

### New to the Azure IoT C SDK?

* **[Ubuntu Telemetry Walkthrough](./doc/ubuntu_telemetry_walkthrough.md):** On Ubuntu, compile a basic  application that sends telemetry to your IoT Hub device.

# C SDK Wiki

For in depth documentation of the C SDK, explore the [Github Wiki](https://github.com/Azure/azure-iot-sdk-c/wiki).

# Components 

* **Azure IoT Hub Device C SDK:** Connect devices running C code to Azure IoT Hub.
* **Azure IoT Hub Service C SDK:** Interface with an Azure IoT Hub service instance from a server-side C application.
* **Azure IoT Hub Provisioning Client SDK:** TODO provisioning_client folder vs provisioning_service_client folder???
* **Azure IoT Hub Device Provisioning Service Client SDK:** Enroll devices with [Azure IoT Device Provisioning Services](https://docs.microsoft.com/azure/iot-dps/) and managing enrollments lists.
* **Serializer Library for C:** A tool to help serialize and deserialize data on your device.


# Packages and Libraries for Device SDK

| Linux   | mbed         | Arduino             | Windows | iOS      |
|---------|--------------|---------------------|---------|----------|
| [apt-get](./iothub_client/readme.md#aptgetpackage) | [MBED library](./iothub_client/readme.md#mbed) | [Arduino IDE Library](./iothub_client/readme.md#arduino) | [NuGet](./iothub_client/readme.md#nugetpackage)   | [CocoaPods](https://cocoapods.org/pods/AzureIoTHubClient) |




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

# Long Term Support

The Azure IoT C SDK offers a Long Term Support (LTS) version is shielded from unwanted changes, while still incorporating critical bugfixes related to security and performance. A new LTS version will be created every 6 months. The lifetime of an LTS branch is currently planned for one year, subject to change by the Azure IoT SDK team. 


| Package | Github Branch | LTS Status | LTS Start Date | Maintenance End Date | Removed Date |
| :-----------: | :-----------: | :--------: | :------------: | :------------------: | :----------: |
| Nuget: 1.1.33<br/> Xenial: 0.1.0.0-35xenial<br/> Trusty: 0.1.0-37trusty<br/>     | lts_01_2018   | Active     | 2018-01-01     | 2018-06-30           | 2018-12-31   |
| 1.x.x         | lts_07_2017   | Deprecated | 2017-07-01     | 2017-12-31           | 2018-06-30   |


---
This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/). For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

[iot-dev-center]: http://azure.com/iotdev
[iot-hub-documentation]: https://docs.microsoft.com/azure/iot-hub/
[devbox-setup]: doc/devbox_setup.md
[setup-iothub]: https://aka.ms/howtocreateazureiothub
[c-sdk-intro]: https://azure.microsoft.com/documentation/articles/iot-hub-device-sdk-c-intro/
[c-porting-guide]: https://github.com/Azure/azure-c-shared-utility/blob/master/devdoc/porting_guide.md
[c-cross-compile]: doc/SDK_cross_compile_example.md
[c-api-reference]: https://azure.github.io/azure-iot-sdk-c/index.html
[azure-iot-sdks]:https://github.com/azure/azure-iot-sdks
