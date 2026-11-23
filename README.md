# Family Link

A React Native (Expo) app that lets parents see where their kids are in real time. Built by our team during the **FII Code 2022** final (Faculty of Computer Science, UAIC Iași).

## How it works

- Parents and kids sign in with Firebase Authentication. Each phone is set up either as a **parent device** or a **kid device**.
- A kid device shows a QR code; the parent scans it to link the two accounts.
- The kid device sends its location (`expo-location`) to Firestore while the app is open. Background tracking with `expo-task-manager` was started but not finished in the time we had.
- The parent sees the list of linked kids and opens each one on a live map (`react-native-maps`).

## Stack

React Native 0.68, Expo SDK 45, React Navigation, Firebase (Auth + Firestore), expo-barcode-scanner, react-native-qrcode-svg.

## Project layout

```
App.js               entry point, navigation container
StackNavigator.js    screen routing
screens/             login, register, form validation
components/          home, add kid (QR), my kids, live map
firebase.js          Firebase config
```

## Run it

```bash
npm install
npx expo start
```

Then open the app in Expo Go on a phone. You need your own Firebase project: put its config in `firebase.js`.
