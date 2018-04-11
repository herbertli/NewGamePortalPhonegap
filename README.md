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
* make sure cordova-plugin-whitelist is installed
```
$ cordova plugin add cordova-plugin-whitelist
$ cordova prepare
```

* Run:
```
$ cordova run ios
```

# TODOS:
- [ ] Add plugins
- [ ] Test for Android
