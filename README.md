
# Angular-Device-Detector
A small library to detect device type, mobile, tablet or desktop

Basic Usage
-----------
include angular.js library in your app:
```html
<script src="//cdnjs.cloudflare.com/ajax/libs/angular.js/1.3.7/angular.min.js"></script>
<script src="device_detector.js"></script>
```

Next, to add **"deviceDetectorModule"** to your Angular app:

```javascript
var app = angular.module("yourApp", ["deviceDetectorModule"]);
```

To use it as directive
```html
<div class="myClass" device-detector></div>
```
* when page is render under mobile device, it will add class **'device-mobile'** into this element.
* when page is rendered under tablet, it will add class **'device-tablet'** into this element.
* when page is render under desktop, it will add class **'device-desktop'** into this element ;
*

To use it as service
```javascript
 angular.module("myApp")
        .service("MyService", ["deviceDetector",function(deviceDetector){
            if (deviceDetector.isDesktop()) {
                // do something
            }
            else if  (deviceDetector.isTablet()) {
                // do something
            }
            else {
                // deviceDetector.isMobile()
                // do something
            }
]);
```