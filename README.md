# Expo Camera onCameraReady unreliability with custom controls

This repository demonstrates a bug in Expo's Camera API related to the `onCameraReady` event. When using custom controls to manage the camera (as opposed to relying solely on Expo's built-in controls), the `onCameraReady` event may not fire consistently, leading to unpredictable camera behavior.

The bug is particularly noticeable after changes in camera permissions or when switching between the front and rear cameras.

## Steps to reproduce

1. Clone this repository.
2. Run `npm install`.
3. Run the app using Expo Go or a similar tool.
4. Observe the camera preview. Note any inconsistencies or blank displays.
5. Toggle camera permissions or switch between front and rear cameras. Observe how the preview behaves. 

## Solution

The solution involves careful handling of the `onCameraReady` event and adding checks for camera availability and permission status before attempting to use the camera.

This repository provides both the buggy code (`bug.js`) and the corrected code (`bugSolution.js`).

## Contributing

Contributions are welcome! Please open an issue or submit a pull request.