# GamePortal Phonegap

## Initial Setup Instructions:
```
cordova create [app-name]
cordova platform add ios
```

## To Run:
* Copy contents of build/ directory from NewGamePortal to www/
* Make sure that in index.html you're calling the correct js file: 
```javascript
<script type="text/javascript" src="static/js/main.be6b2d5f.js"></script>
```

* Before that line add:
```javascript
<script type="text/javascript" src="cordova.js"></script>
```

```
cordova run ios
```
