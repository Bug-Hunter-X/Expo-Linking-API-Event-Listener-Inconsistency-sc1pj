# Expo Linking API Event Listener Inconsistency

This repository demonstrates a bug in the Expo `Linking` API where the `Linking.addEventListener` method may not consistently fire, particularly when the app is in the background or has been terminated. This can result in deep links not being handled properly.

## Bug Reproduction

1. Clone this repository.
2. Run the project using `expo start`.
3. Send a deep link to the app (e.g., using a different app or browser).
4. Observe that the event listener may not always be triggered, particularly when the app is not active.

## Solution

The `LinkingBugSolution.js` file provides a workaround to improve the reliability of the deep link handling. This involved checking for initial URLs on app load and using a more robust approach to managing the event listener.