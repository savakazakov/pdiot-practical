# Week 3 Lab

# Contents 
- introduction to Android Development
- understanding sensor data processing code 
- Tensorflow and TFLite
- resources on how to run a TFLite model on device

# Introduction

This week we will introduce you to some Android development concepts and Bluetooth Low Energy (BLE). 
Your task will be to start using the [TFLite](https://www.tensorflow.org/lite) package to perform real-time human activity recognition on the mobile phone.

# Android
Your future Android app should interface with the sensor of your choice (Respeck or Thingy) using Bluetooth LE and provide a user interface showing the activity prediction.

You already have access to a basic app which can be used to record sensor data for offline analysis. You are free to use this app as a starting point for your own application.

## 1. If you don't already have it - Install Android Studio

It is recommended that you use Android Studio. The IDE can be downloaded from [here](https://developer.android.com/studio/).

## 2. Phone

We use Xiaomi Redmi 4A or 5A phones and can lend one if required. Other phones may work for the practical but there can be Bluetooth compatibility issues with other devices. Please let the demonstrators know if your device is not working.

## 3. Android programming basics

There are multiple resources online that will give you a good, quick introduction to Android programming. We suggest [this tutorial](https://google-developer-training.github.io/android-developer-fundamentals-course-concepts-v2/) which covers all the basics you will need for this course. 

## 4. BLE Introduction

Bluetooth Low Energy (BLE) provides wireless communications for low power devices. 
Devices advertise one or more services, which themselves contain a number of characteristics. 
For example, a heart rate monitor may provide a service which contains a characteristic which 
will send the current pulse rate. Characteristics can either be readable, writable or 
allow notifications, which means that new data will be streamed over BLE when it is available. 
This is the mode that we use to send accelerometer and gyroscope data from the Respeck and Thingy.

A good explanation of the BLE system can be found [here](https://learn.adafruit.com/introduction-to-bluetooth-low-energy/introduction).

## 5. BLE on Android

As mentioned previously, the repository contains the PDIoT data collection app, which you can use as an example of BLE communication on Android. We use the [RXAndroidBLE](https://polidea.github.io/RxAndroidBle) library which simplifies much of the communication code. Note that this requires Java 8 support (enabled in build.gradle as shown below).

build gradle:

```java
android {
        compileOptions {
            sourceCompatibility JavaVersion.VERSION_1_8
            targetCompatibility JavaVersion.VERSION_1_8
            }
}
```

## 6. Permissions

To make the data collection app work correctly, you&#39;ll need to enable _location_ and _storage_ permissions in _settings/apps/permissions_. Location permissions is required when scanning for BLE devices. If you don&#39;t have this you&#39;ll see a _BLE Scanning Error_ message when starting the app.

## 7. Where to look for code

You have the entire codebase of the PDIoT app to take inspiration from. Some important files are:
- bluetooth/BluetoothSpeckService.kt -> the main Bluetooth service. This is where we scan for devices, connect to the relevant ones and start the processing of each packet of data
- utils/ThingyPacketDecoder.kt and utils/RespeckPacketDecoder.kt -> functions that decode the raw packet data into actual accel, gyro and mag values
- utils/RespeckPacketHandler.kt and utils/ThingyPacketHandler.kt -> where you might want to start processing your data for classification
- bluetooth/LiveDataActivity.kt -> the live data activity where you can see real-time graphs of the accelerometer data coming from both sensors. 

In particular, [this line](https://github.com/specknet/pdiotapp/blob/update_2021/app/src/main/java/com/specknet/pdiotapp/live/LiveDataActivity.kt#L61)
in the LiveDataActivity file is where we listen for updates from the Respeck. A similar piece of code
can be seen lower for the data coming from the Thingy. This would also be a good place where you can start 
buffering data to form your sliding windows and send them to your chosen classifier.

## 8. Importing a TFLite model on the phone

After you train an early iteration of your HAR model with Tensorflow, you will be able to [export it to a .tflite format](https://www.tensorflow.org/lite/convert#converting_a_savedmodel_).

You can find a lot of examples of on-device prediction using TFLite [here](https://www.tensorflow.org/lite/examples).
We recommend starting with the [Audio classification](https://www.tensorflow.org/lite/examples/audio_classification/overview)
as it is similar in many ways to classification of sensor data.

If you are using the sliding window approach for classification you will have to progressively save data into a list on the app. Once the list becomes full, you can pass its contents to your classifier. 

## 9. Exploring other ways of classification

If you will be doing hierarchical classification or mixing up types of models, you can look into [importing sklearn trained models](https://github.com/jpmml/sklearn2pmml) into an Android app. You may also consider setting up a backend where all your classification can take place rather than force all classification to happen on the phone

# More resources
Check out the following links for more information about:
* [Android development](https://developer.android.com/training/basics/firstapp)
* [TFLite for Android](https://www.tensorflow.org/lite/examples)
* [Bluetooth Low Energy](https://developer.android.com/guide/topics/connectivity/bluetooth-le)
* [More BLE](https://www.bluetooth.com/bluetooth-resources/intro-to-bluetooth-low-energy/)
