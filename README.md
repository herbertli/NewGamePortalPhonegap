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
npm run build
```

### NewGamePortalPhonegap Checklist 
* Copy contents of NewGamePortal/build/ directory to www/
* Make sure that in index.html you're calling the correct js file (change static/js/main.be6b2d5f.js to the actual js file in static/js/): 
```javascript
<script type="text/javascript" src="static/js/main.be6b2d5f.js"></script>
```

* Before that line add:
```javascript
<script type="text/javascript" src="cordova.js"></script>
```

* Run:
```
cordova run ios
```

# TODOS:
- [ ] Add plugins
- [ ] Test for Android
