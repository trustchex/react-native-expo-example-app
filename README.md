# React Native Expo Example App

This is a new [**React Native**](https://reactnative.dev) project, bootstrapped using [**Expo**](https://expo.dev) with the TrustChex SDK integration.

## Getting Started

>**Note**: Make sure you have completed the [React Native - Environment Setup](https://reactnative.dev/docs/environment-setup) instructions till "Creating a new application" step, before proceeding.

### Step 1: Install dependencies

First, you will need to install the project dependencies:

```bash
# using npm
npm install

# OR using Yarn
yarn install
```

### Step 2: Start the Metro Server

You will need to start **Metro**, the JavaScript _bundler_ that ships _with_ React Native.

To start Metro, run the following command from the _root_ of your React Native project:

```bash
# using npm
npm start

# OR using Yarn
yarn start
```

### Step 3: Start your Application

Let Metro Bundler run in its _own_ terminal. Open a _new_ terminal from the _root_ of your React Native project. Run the following command to start your _Android_ or _iOS_ app:

#### For Android

```bash
# using npm
npm run android

# OR using Yarn
yarn android
```

#### For iOS

```bash
# using npm
npm run ios

# OR using Yarn
yarn ios
```

#### For Web

```bash
# using npm
npm run web

# OR using Yarn
yarn web
```

If everything is set up _correctly_, you should see your new app running in your _Android Emulator_, _iOS Simulator_, or _web browser_ shortly provided you have set up your emulator/simulator correctly.

This is one way to run your app — you can also run it directly from within Android Studio and Xcode respectively.

## Step 4: Modifying your App

Now that you have successfully run the app, let's modify it.

1. Open `app/index.tsx` in your text editor of choice and edit some lines.
2. For **Android**: Press the <kbd>R</kbd> key twice or select **"Reload"** from the **Developer Menu** (<kbd>Ctrl</kbd> + <kbd>M</kbd> (on Window and Linux) or <kbd>Cmd ⌘</kbd> + <kbd>M</kbd> (on macOS)) to see your changes!

   For **iOS**: Hit <kbd>Cmd ⌘</kbd> + <kbd>R</kbd> in your iOS Simulator to reload the app and see your changes!

## Expo Specifics

This project uses Expo with the following configuration:

- **Expo SDK**: 53.0.20
- **Expo Router**: File-based routing system
- **New Architecture**: Enabled for Fabric and TurboModules support

### Expo Development Build

This project supports Expo development builds. You can create a development build by running:

```bash
npx expo run:android
npx expo run:ios
```

### EAS Build (Optional)

For cloud builds, you can use EAS Build:

```bash
npm install -g eas-cli
eas build --platform all
```

## Project Structure

```
├── app/                    # Expo Router pages
│   ├── _layout.tsx        # Root layout
│   ├── index.tsx          # Home screen
│   └── +not-found.tsx    # 404 page
├── assets/                # Static assets
├── components/            # Reusable components
├── constants/             # App constants
├── hooks/                 # Custom hooks
├── android/               # Native Android code
├── ios/                   # Native iOS code
├── app.json              # Expo configuration
├── babel.config.js       # Babel configuration
├── metro.config.js       # Metro bundler configuration
└── tsconfig.json         # TypeScript configuration
```

## Features

- **TrustChex SDK**: Document verification and identity validation
- **Camera Integration**: react-native-vision-camera for document scanning
- **Deep Linking**: Custom URL scheme support
- **TypeScript**: Full TypeScript support
- **SVG Support**: Vector graphics with react-native-svg
- **Animations**: Smooth animations with react-native-reanimated

## Troubleshooting

If you can't get this to work, see the [Troubleshooting](https://reactnative.dev/docs/troubleshooting) page.

### Common Expo Issues

- **Metro bundler issues**: Try clearing the cache with `npx expo start --clear`
- **iOS build issues**: Make sure you have Xcode and iOS Simulator installed
- **Android build issues**: Ensure Android Studio and SDK are properly configured

## Learn More

To learn more about React Native and Expo, take a look at the following resources:

- [React Native Website](https://reactnative.dev) - learn more about React Native.
- [Expo Documentation](https://docs.expo.dev) - learn about Expo features and API.
- [Getting Started](https://reactnative.dev/docs/environment-setup) - an **overview** of React Native and how setup your environment.
- [Learn the Basics](https://reactnative.dev/docs/getting-started) - a **guided tour** of the React Native **basics**.
- [Blog](https://reactnative.dev/blog) - read the latest official React Native **Blog** posts.
- [`@facebook/react-native`](https://github.com/facebook/react-native) - the Open Source; GitHub **repository** for React Native.
