# Firebase Authentication Bug: onAuthStateChanged Listener Delay and Error Handling

This repository demonstrates a common issue with Firebase authentication: a delay in the `onAuthStateChanged` listener triggering after successful sign-in, coupled with a lack of comprehensive error handling. This can lead to unexpected behavior in your application.

The `firebaseAuthBug.js` file showcases the problem.  The `firebaseAuthSolution.js` file provides a solution that addresses the delay and adds more robust error handling.

## Setup

1.  Clone this repository.
2.  Install Firebase: `npm install firebase`
3.  Configure your Firebase project and add your configuration to `firebaseConfig.js` (you'll need to create this file).
4.  Run the application using `node firebaseAuthBug.js` (and then `node firebaseAuthSolution.js`) to observe the behavior.

## Problem

The original code suffers from a race condition and lacks detailed error reporting which makes it very hard to resolve what is happening when the sign in fails.