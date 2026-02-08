# React Native Expo Example App

This is a [**React Native**](https://reactnative.dev) project, bootstrapped using [**Expo**](https://expo.dev) with the **TrustChex SDK** integration for identity verification and document validation.

## Prerequisites

Before getting started, ensure you have the following installed:

- **Node.js** (v18 or later)
- **npm** or **Yarn**
- **Expo CLI** (`npm install -g @expo/cli`)
- **Android Studio** (for Android development)
- **Xcode** (for iOS development, macOS only)

>**Note**: Make sure you have completed the [React Native - Environment Setup](https://reactnative.dev/docs/environment-setup) instructions till "Creating a new application" step, before proceeding.

## Getting Started

### Step 1: Clone and Install Dependencies

First, you will need to install the project dependencies:

```bash
# using npm
npm install

# OR using Yarn
yarn install
```

### Step 2: Start the Development Server

To start the Expo development server, run the following command from the root of your project:

```bash
# using npm
npm start

# OR using Yarn
yarn start

# OR using Expo CLI directly
npx expo start
```

### Step 3: Run Your Application

#### For Android

```bash
# using npm
npm run android

# OR using Yarn
yarn android

# OR using Expo CLI directly
npx expo run:android
```

#### For iOS

```bash
# using npm
npm run ios

# OR using Yarn
yarn ios

# OR using Expo CLI directly
npx expo run:ios
```

> **Note**: This app requires native device capabilities (camera and NFC) and is not compatible with web browsers. You must run it on physical devices or simulators.

If everything is set up correctly, you should see your new app running in your Android Emulator or iOS Simulator shortly provided you have set up your emulator/simulator correctly.

This is one way to run your app — you can also run it directly from within Android Studio and Xcode respectively.

## Step 4: Modifying your App

Now that you have successfully run the app, let's modify it.

1. Open `app/index.tsx` in your text editor of choice and edit some lines.
2. For **Android**: Press the **R** key twice or select **"Reload"** from the **Developer Menu** (**Ctrl + M** on Windows and Linux or **Cmd ⌘ + M** on macOS) to see your changes!

   For **iOS**: Hit **Cmd ⌘ + R** in your iOS Simulator to reload the app and see your changes!

## Expo Configuration

This project uses Expo with the following configuration:

- **Expo SDK**: ~53.0.20
- **React Native**: 0.79.5
- **React**: 19.0.0
- **Expo Router**: File-based routing system (~5.1.4)
- **New Architecture**: Enabled for Fabric and TurboModules support
- **TypeScript**: Full TypeScript support (~5.8.3)

### Deep Linking

The app supports deep linking with the custom URL scheme: `reactnativeexpoexampleapp://`

### Required Permissions

#### iOS

- Camera access for document and face capture
- Microphone access for video recording
- NFC reading for document verification

#### Android

- `INTERNET` - Network access
- `CAMERA` - Document and face capture
- `NFC` - Document verification
- `RECORD_AUDIO` - Video recording with audio
- `VIBRATE` - Haptic feedback

### Expo Development Build

This project supports Expo development builds. You can create a development build by running:

```bash
npx expo run:android
npx expo run:ios
```

### EAS Build (Optional)

For cloud builds, you can use EAS Build for Android and iOS:

```bash
npm install -g eas-cli
eas build --platform android
eas build --platform ios
```

> **Note**: Web builds are not supported due to camera and NFC dependencies.

## Project Structure

```text
├── app/                    # Expo Router pages
│   ├── _layout.tsx        # Root layout
│   ├── index.tsx          # Home screen (TrustChex integration)
│   └── +not-found.tsx    # 404 page
├── assets/                # Static assets
│   ├── fonts/             # Custom fonts
│   └── images/            # App icons and images
├── components/            # Reusable React components
│   ├── ui/               # UI-specific components
│   ├── Collapsible.tsx
│   ├── ExternalLink.tsx
│   ├── HapticTab.tsx
│   ├── HelloWave.tsx
│   ├── ParallaxScrollView.tsx
│   ├── ThemedText.tsx
│   └── ThemedView.tsx
├── constants/             # App constants and themes
├── hooks/                 # Custom React hooks
├── android/               # Native Android code
├── ios/                   # Native iOS code
├── scripts/               # Build and utility scripts
├── app.json              # Expo configuration
├── babel.config.js       # Babel configuration
├── metro.config.js       # Metro bundler configuration
├── tsconfig.json         # TypeScript configuration
└── package.json          # Dependencies and scripts
```

## Features

- **TrustChex SDK**: Document verification and identity validation (`@trustchex/react-native-sdk`)
- **Camera Integration**: `react-native-vision-camera` for document scanning and video recording
- **Deep Linking**: Custom URL scheme support with `expo-linking`
- **TypeScript**: Full TypeScript support with strict type checking
- **NFC Support**: NFC document reading with `react-native-nfc-manager`
- **Image Processing**: Image editing with `@react-native-community/image-editor`
- **Video Compression**: Video optimization with `react-native-compressor`
- **Computer Vision**: OpenCV integration with `react-native-fast-opencv`
- **File System**: File operations with `react-native-fs`
- **Text-to-Speech**: Audio feedback with `react-native-tts`
- **SVG Support**: Vector graphics with `react-native-svg`
- **Animations**: Smooth animations with `react-native-svg` and Lottie
- **Gestures**: Touch handling with `react-native-gesture-handler`

> **Platform Support**: This app is designed for **mobile platforms only** (Android and iOS). Web support is not available due to camera and NFC hardware requirements.

## Troubleshooting

### Common Issues

#### Expo/Metro Issues

- **Metro bundler cache issues**: Try clearing the cache with `npx expo start --clear`
- **Node modules issues**: Delete `node_modules` and run `npm install` again
- **Expo CLI version**: Ensure you're using the latest Expo CLI: `npm install -g @expo/cli`

#### iOS Build Issues

- **Xcode requirements**: Make sure you have Xcode 14+ installed
- **iOS Simulator**: Ensure iOS Simulator is properly configured
- **Cocoapods issues**: Try `cd ios && pod install` if using bare workflow
- **iOS deployment target**: Minimum iOS version is 16.0

#### Android Build Issues

- **Android Studio setup**: Ensure Android Studio and SDK are properly configured
- **Java version**: Use Java 17 for optimal compatibility
- **Gradle issues**: Try cleaning with `cd android && ./gradlew clean`
- **Device permissions**: Ensure camera and NFC permissions are granted

#### TrustChex SDK Issues

- **Camera permissions**: Verify camera permissions are granted in device settings
- **NFC availability**: NFC is only available on physical devices, not simulators
- **Network connectivity**: Ensure stable internet connection for API calls
- **Deep linking**: Test deep linking with a proper session URL

For more help, see the [Troubleshooting](https://reactnative.dev/docs/troubleshooting) page.

### Development Tools

```bash
# Reset project to initial state
npm run reset-project

# Lint code
npm run lint

# Clear all caches
npx expo start --clear --reset-cache
```

## Learn More

To learn more about React Native and Expo, take a look at the following resources:

- [React Native Website](https://reactnative.dev) - learn more about React Native.
- [Expo Documentation](https://docs.expo.dev) - learn about Expo features and API.
- [Getting Started](https://reactnative.dev/docs/environment-setup) - an **overview** of React Native and how setup your environment.
- [Learn the Basics](https://reactnative.dev/docs/getting-started) - a **guided tour** of the React Native **basics**.
- [Blog](https://reactnative.dev/blog) - read the latest official React Native **Blog** posts.
- [`@facebook/react-native`](https://github.com/facebook/react-native) - the Open Source; GitHub **repository** for React Native.
