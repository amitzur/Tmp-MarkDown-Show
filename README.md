
# Examples

## via Configuration

The examples use `@applitools/eyes-selenium` but are relevant also for webdriver.io and protractor SDK's.

### Using single iOS device via `addBrowser`

```js
const {IosDeviceName, IosScreenOrientation} = require('@applitools/eyes-selenium')
// ...
configuration.addBrowser({
  iosDeviceInfo: {
    deviceName: IosDeviceName.iPhone_11,
    screenOrientation: IosScreenOrientation.LANDSCAPE_LEFT,
  },
})
```

### multiple devices via `addBrowsers`
```js
const {IosDeviceName, IosScreenOrientation} = require('@applitools/eyes-selenium')
// ...
configuration.addBrowsers(
    {
      iosDeviceInfo: {
        deviceName: IosDeviceName.iPhone_11,
        screenOrientation: IosScreenOrientation.LANDSCAPE_LEFT,
      },
    },
    {
      iosDeviceInfo: {
        deviceName: IosDeviceName.iPhone_7,
        screenOrientation: IosScreenOrientation.PORTRAIT,
      },
    },
  )
```

### chrome emulation - existing
```js
const {ScreenOrientation, DeviceName} = require('@applitools/eyes-selenium')
// ...
configuration.addBrowser({
    deviceName: DeviceName.iPhone_XS,
    screenOrientation: ScreenOrientation.PORTRAIT,
  })
```

### chrome emulation - new (like iosDeviceInfo)
```js
const {ScreenOrientation, DeviceName} = require('@applitools/eyes-selenium')
// ...
configuration.addBrowser({
      chromeEmulationInfo: {
        deviceName: DeviceName.iPhone_6_7_8,
        screenOrientation: ScreenOrientation.PORTRAIT,
      },
    })
```


### desktop - existing
```js
const {BrowserType} = require('@applitools/eyes-selenium')
// ...
configuration.addBrowser({
  name: BrowserType.EDGE_CHROMIUM_TWO_VERSIONS_BACK,
  width: 768,
  height: 1024,
})
```
