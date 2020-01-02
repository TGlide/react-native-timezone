# React Native Timezone
A Simple react native module to get Timezone of the Android/iOS device.

# Motivation
For a project of mine, I had to acquire the current selected timezone of the user. But unfortunately I could not find any react native package or react native in-build function which facilitates this. Thus I created a small library.

# Compatibility
| React native version | Tested | Result |
|----------------------|--------|--------|
| < 0.60.0             |   ❓   |   ❓   |
| >= 0.60.0            |   ✅   |   ✅   |

NOTE: Currently I've only tested this library with RN projects >= 0.60.0. If you tested this with older versions of RN, please let me know the status. 

# Installation
 
 For RN version >= 0.60.0,
 
 `npm i --save react-native-timezone`
 
 ## iOS
 `cd ios/ && pod install`
 
 ## Android
 Nothing else to do after npm install.
 
 # Usage
 ```javascript
import TimeZone from 'react-native-timezone';

getTimeZone = async() => {
  const timeZone = await TimeZone.getTimeZone().then(zone => zone);
  console.log({ timeZone });
}
```

 # API
| API         | Description                                                                                                                                                 |
|-------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getTimeZone | Android : Returns timezone ID using java.util.TimeZone.getID()<br>iOS : This always reflects the current system time zone using localTimeZone of NSTimeZone |
