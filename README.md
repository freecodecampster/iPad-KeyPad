# iPad-KeyPad
 Send keystrokes from an iPad Xcode Playground to Windows/Mac desktops
 
 ![Playground Screenshot](https://github.com/freecodecampster/iPad-KeyPad/blob/master/images/screenshot.PNG)
 
## Purpose
Demonstrate use of Swift, SwiftUI, and Network API to send keystrokes across a local network to a computer hosting Vicreo Listener. https://jeffreydavidsz.github.io/VICREO-Listener/

## Description

The playground example is set up to send commands to the game Civilization IV. Hopefully, this demonstrates the flexibility of SwiftUI Playgrounds to create custom interfaces for your favourite applications.

The Vicreo Listener GitHub pages describes what messages it can receive. It receives on TCP port 10001 and the IP address for the playground to send to is set in TCPClient.swift found in the sources folder of the playground. On Windows type ipconfig at a command prompt to discover your computer's IP address.

The singleton pattern is used extensively in this Swift playground.

I couldn't really find much sample code on using Network Connections-NWConnection with Swift online, so hopefully the code here might be useful. Particularly, I found that to communicate with Vicreo Listener it is essential to send a TCP message with the isComplete argument set to false that is until you want to terminate the connection which can be done by clicking the trashcan icon.

To keep the playground from slowing down I discovered that placing the Swift UI code for the buttons into separate swift files and placing these in the sources folder allows the compiler to precompile these files as it knows these won't be edited during execution. These Swift UI views are called in the main body View.

Various button styles are also in the sources folder.

## Requirements

iPad running iOS 13 Playgrounds
Windows or Mac Desktop
Vicreo Listener. https://jeffreydavidsz.github.io/VICREO-Listener/


## Test Environment
iPad Pro 9.7 running iOS 13 Playgrounds
Windows 10 v1909
Local Wireless Network

## Results 
Very quick from button press to executing the key press on desktop. Playgrounds have a very small file size. Robust, reliable communication with Network API.
