# Indoor Localization

This project explores Indoor Localization with **Sensor Fusion** of **PDR** (Pedestrian Dead Reckoning) and a **Single RTT**
(Round Trip Time) **Wi-Fi** with **known initial position**, the implementation of which deals with **IMU**
measurements, **Complementary Filters** and **Kalman Filters**.

It is a project on Indoor Localization without using trilaterization and using as
less dependencies as possible ( Range information from 1 AP and 1 IMU ). Since
a single range equation would give many solutions the location of the starting
point is assumed as known. This can be a valid assumption in many cases.

The aim is also to make a prototype app running on Android which could be used for
helping Visually Challenged people navigate their surroundings in a public place.

## Application Examples

### Supermarket Cart Location Analysis

The problem is to track the Carts in supermarkets so that we can gather
information about what consumers are doing the data obtained can then be
used in Data Analysis and Machine Learning Models to gather useful
information.

### Localization for the Visually Impaired in Public Places

Here the problem is to track the location of Visually Impaired person, so that
directions can be given to them using a speech assistant when they find themselves
in a new location.

## Simulation
<img src='https://user-images.githubusercontent.com/64144419/126338954-00fe2cc0-0a84-4ea5-b742-f3ab3fdf24f1.png' width=600>

## Android App
<img src='https://user-images.githubusercontent.com/64144419/126339944-15344624-19af-4d6b-9593-7fc2dc487c9d.png' width=200>

For more details on each of these, checkout the main [Report](./Indoor_Localization_CS6650_Report.pdf) and README's in each of the folders.

