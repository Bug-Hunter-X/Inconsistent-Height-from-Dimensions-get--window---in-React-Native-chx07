# React Native Dimensions.get('window') Height Inconsistency

This repository demonstrates a bug where `Dimensions.get('window')` in React Native returns an unexpectedly small height value, particularly on Android devices.  The issue is related to inconsistencies in how the window dimensions are reported, potentially influenced by system UI elements or device configurations.

## Problem

The `Dimensions.get('window').height` value is often smaller than the actual screen height, leading to layout problems.  The provided code shows how the reported height is inconsistent and smaller than expected, causing components to be rendered incorrectly.

## Solution

The solution involves using the `react-native-safe-area-context` library which handles the inclusion of system UI elements correctly.  It provides accurate dimensions that take into account the status bar, navigation bar and other safe area insets.  This ensures components are rendered properly within the usable screen area.

## Setup

1. Clone this repository.
2.  Install the necessary dependencies:  `npm install` or `yarn install`
3. Run the app: `npx react-native run-android` (or `npx react-native run-ios`)

Compare the layout and height values in the `DimensionsBug.js` and `DimensionsBugSolution.js` examples to see the difference the solution makes.