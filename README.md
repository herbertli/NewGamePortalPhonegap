# GamePortal Phonegap

## Initial Setup Instructions:
```
cordova create [app-name]
cordova platform add ios
```

## To Run:

### NewGamePortal Checklist:
* Make sure you are using HashRouter instead of BrowserRouter
* Make sure you add cordova to global window object and listen to 'deviceready' event
```typescript
declare global {
  interface Window { cordova: any; }
}

if (window.cordova) {
  document.addEventListener('deviceready', reactRender, false);
} else {
  reactRender();
}
```
```
$ npm run build
```

### NewGamePortalPhonegap Checklist 
* make sure following plugins are installed ($ cordova plugin add [plugin name]):
  * cordova-plugin-whitelist
  * cordova-sms-plugin
  * cordova-plugin-contacts
  * cordova-universal-links-plugin
* cordova-universal-links-plugin breaks in iOS, use this fix: https://github.com/martindrapeau/cordova-universal-links-plugin/commit/b0f85438e4ef9d107be0aadeb218ae9c4131d02a#diff-084a996a8428527995ef522579929873

* Run:
```
$ cordova run ios
```

# TODOS:
- [ ] Add plugins
- [ ] Test for Android
