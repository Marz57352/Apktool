### Apktool
_This is the repository for Apktool. The website is at the [apktool.org](https://github.com/iBotPeaches/apktool.org) repository._

[![CI](https://github.com/iBotPeaches/Apktool/actions/workflows/build.yml/badge.svg)](https://github.com/iBotPeaches/Apktool/actions/workflows/test.yml)
[![Software License](https://img.shields.io/badge/license-Apache%202.0-brightgreen.svg)](https://github.com/iBotPeaches/Apktool/blob/master/LICENSE.md)

Apktool is a tool for reverse engineering third-party, closed, binary, Android apps. It can decode resources to nearly original form and rebuild them after making some modifications; it makes it possible to debug smali code step-by-step. It also makes working with apps easier thanks to project-like file structure and automation of some repetitive tasks such as building apk, etc.

Apktool is **NOT** intended for piracy and other non-legal uses. It could be used for localizing and adding features, adding support for custom platforms, and other GOOD purposes. Just try to be fair with the authors of an app, that you use and probably like.

#### Support
- [Project Page](https://apktool.org)
- [#apktool on libera.chat](https://web.libera.chat)

#### Security Vulnerabilities

If you discover a security vulnerability within Apktool, please send an e-mail to Connor Tumbleson at connor.tumbleson(at)gmail.com. All security vulnerabilities will be promptly addressed.

#### Links
- [Downloads](https://bitbucket.org/iBotPeaches/apktool/downloads)
- [Downloads Mirror](https://connortumbleson.com/apktool)
- [How to Build](https://apktool.org/docs/build)
- [Documentation](https://apktool.org/wiki/the-basics/intro)
- [Bug Reports](https://github.com/iBotPeaches/Apktool/issues)
- [Changelog/Information](https://apktool.org/blog)
- [XDA Post](https://forum.xda-developers.com/t/util-dec-2-2020-apktool-tool-for-reverse-engineering-apk-files.1755243/)
- [Source (GitHub)](https://github.com/iBotPeaches/Apktool)
- [Source (Bitbucket)](https://bitbucket.org/iBotPeaches/apktool/)


## Sponsors

Special thanks goes to the following sponsors:

### Sourcetoad
[Sourcetoad](https://sourcetoad.com/) is an award-winning software and app development firm committed to the co-creation of technology solutions that solve complex business problems, delight users, and help our clients achieve their goals.

<a href="https://www.sourcetoad.com" alt="Sourcetoad">
    <picture>
        <img src="https://github.com/ibotpeaches/apktool/raw/master/.github/assets/sponsors/sourcetoad-horizontal.svg">
    </picture>
</a>

### Emerge Tools

[Emerge Tools](https://www.emergetools.com) is a suite of revolutionary products designed to supercharge mobile apps and the teams that build them.

<a href="https://www.emergetools.com" alt="Emerge Tools">
    <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://github.com/ibotpeaches/apktool/raw/master/.github/assets/sponsors/emerge-tools-vertical-white.svg">
        <source media="(prefers-color-scheme: light)" srcset="https://github.com/ibotpeaches/apktool/raw/master/.github/assets/sponsors/emerge-tools-vertical-black.svg">
        <img src="https://github.com/ibotpeaches/apktool/raw/master/.github/assets/sponsors/emerge-tools-vertical-black.svg">
    </picture>
</a>>// App.js (Main entry point for GTS - Guide to Survive)
import React from 'react';
import { SafeAreaView, StyleSheet, StatusBar } from 'react-native';
import { NavigationContainer } from '@react-navigation/native';
import { createBottomTabNavigator } from '@react-navigation/bottom-tabs';
import { Ionicons } from '@expo/vector-icons';

import HomeScreen from './screens/HomeScreen';
import ToolsScreen from './screens/ToolsScreen';
import DetectAIScreen from './screens/DetectAIScreen';
import SurvivalScreen from './screens/SurvivalScreen';
import SettingsScreen from './screens/SettingsScreen';

const Tab = createBottomTabNavigator();

export default function App() {
  return (
    <NavigationContainer>
      <StatusBar barStyle="light-content" />
      <SafeAreaView style={styles.container}>
        <Tab.Navigator
          screenOptions={({ route }) => ({
            tabBarIcon: ({ color, size }) => {
              let iconName = '';
              if (route.name === 'Home') iconName = 'home';
              else if (route.name === 'Tools') iconName = 'construct';
              else if (route.name === 'Detect AI') iconName = 'scan-circle';
              else if (route.name === 'Survival') iconName = 'leaf';
              else if (route.name === 'Settings') iconName = 'settings';
              return <Ionicons name={iconName} size={size} color={color} />;
            },
            tabBarActiveTintColor: 'limegreen',
            tabBarInactiveTintColor: 'gray',
            headerShown: false,
          })}
        >
          <Tab.Screen name="Home" component={HomeScreen} />
          <Tab.Screen name="Tools" component={ToolsScreen} />
          <Tab.Screen name="Detect AI" component={DetectAIScreen} />
          <Tab.Screen name="Survival" component={SurvivalScreen} />
          <Tab.Screen name="Settings" component={SettingsScreen} />
        </Tab.Navigator>
      </SafeAreaView>
    </NavigationContainer>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#000',
  },
});

// screens/HomeScreen.js
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

const HomeScreen = () => {
  return (
    <View style={screenStyles.container}>
      <Text style={screenStyles.text}>Welcome to GTS – Guide to Survive</Text>
    </View>
  );
};

export default HomeScreen;

// screens/ToolsScreen.js
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

const ToolsScreen = () => {
  return (
    <View style={screenStyles.container}>
      <Text style={screenStyles.text}>Toolkits for survival, engineering, chemistry, and more</Text>
    </View>
  );
};

export default ToolsScreen;

// screens/DetectAIScreen.js
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

const DetectAIScreen = () => {
  return (
    <View style={screenStyles.container}>
      <Text style={screenStyles.text}>AI Detection Interface (Text, Image, Video, Audio)</Text>
    </View>
  );
};

export default DetectAIScreen;

// screens/SurvivalScreen.js
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

const SurvivalScreen = () => {
  return (
    <View style={screenStyles.container}>
      <Text style={screenStyles.text}>Outdoor survival, rebuilding society, apocalypse guides</Text>
    </View>
  );
};

export default SurvivalScreen;

// screens/SettingsScreen.js
import React from 'react';
import { View, Text, StyleSheet } from 'react-native';

const SettingsScreen = () => {
  return (
    <View style={screenStyles.container}>
      <Text style={screenStyles.text}>Settings: Offline access, memory folders, voice access</Text>
    </View>
  );
};

export default SettingsScreen;

const screenStyles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    backgroundColor: '#000',
    padding: 20,
  },
  text: {
    color: 'limegreen',
    fontSize: 18,
    textAlign: 'center',
  },
});

