# Intelligent Dead Reckoning (IDR) System

## About the Program
This repository contains the codebase for an AI-ML based Intelligent Dead Reckoning (IDR) system designed for seamless navigation during GNSS (GPS) blackouts. It addresses the Smart India Hackathon (SIH) problem statement 20768 provided by the Indian Space Research Organisation (ISRO).

The system transforms a standalone smartphone into an intelligent navigation device. It utilizes the phone's internal Inertial Measurement Unit (IMU) sensors (accelerometer, gyroscope) to track a vehicle's position via dead reckoning when external GNSS signals fail (e.g., in long underground tunnels or deep urban canyons). 

Using machine learning and sensor fusion (GNSS+INS), the software filters out non-navigation noise such as engine vibrations and potholes, calculates distance and velocity, and ensures an instant, seamless transition between satellite tracking and inertial tracking to maintain continuous, highly accurate navigation.
