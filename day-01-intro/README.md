# Day 1: Getting Started with Cisco Packet Tracer

**Course:** Jeremy's IT Lab, CCNA 200-301 v1.1
**Date:** October 2026

## Goal
Set up Cisco Packet Tracer so I can practice labs for the rest of the CCNA course.

## What I did
- Downloaded and installed Cisco Packet Tracer
- Signed in with my Cisco Networking Academy account
- Opened the app and got familiar with the workspace

## Problems I ran into
**Login error: Packet Tracer could not open port 8001.**
- Packet Tracer needs port 8001 on my computer to complete the browser login.
- I found what was using it with `netstat -ano | findstr :8001`, which showed a process ID.
- I identified the process with `tasklist /FI "PID eq <PID>"`. It was `splunkd.exe`, a Splunk service that starts automatically with Windows.
- I stopped Splunk, confirmed the port was free, and signed in successfully.
- To prevent it from happening again, I set the Splunk service to start manually.

## What I learned
- How to check which program is using a network port on Windows
- Services can run in the background and block other applications from using a port

## Config
No device configuration in this lab.