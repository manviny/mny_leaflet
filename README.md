##How to create a new angular component (bower)
[Brian Ford](http://briantford.com/blog/angular-bower)  

## install it
bower install manviny/mny_leaflet --save


mny_leaflet
===========

```html
<ons-page class="center" ng-controller="LocalizaCtrl">
    <leaflet center="centerHere" markers="myMarkers"  layers="layers" defaults="defaults"  ></leaflet>
</ons-page>
````


```javascript
angular.module('myApp')
  .controller('LocalizaCtrl', function ($scope, mnymapa) {

  	// initialize map
	mnymapa.setDefaultMap();


  	var array = [];
	// array.push({lat: 39.50300178969824, lng: -3.878173828125, focus: true, draggable: false});	
	// array.push({lat: 38.50300178969824, lng: -2.878173828125, focus: true, draggable: false});	

	mnymapa.pushMarkers(array); 
	mnymapa.myPosition();
	// mnymapa.fitMarkers(array); // not reloading map

  });
```


