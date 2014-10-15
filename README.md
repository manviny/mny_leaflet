##How to create a new angular component (bower)
[Brina Ford](http://briantford.com/blog/angular-bower)


mny_leaflet
===========

```html
<ons-page class="center" ng-controller="LocalizaCtrl">
    <leaflet center="centerHere" markers="myMarkers"  layers="layers" defaults="defaults"  ></leaflet>
</ons-page>
````


```javascript
angular.module('myApp')
  .controller('LocalizaCtrl', function ($scope, mapa) {

  	// initialize map
	mapa.setDefaultMap();


  	var array = [];
	// array.push({lat: 39.50300178969824, lng: -3.878173828125, focus: true, draggable: false});	
	// array.push({lat: 38.50300178969824, lng: -2.878173828125, focus: true, draggable: false});	

	mapa.pushMarkers(array); 
	mapa.myPosition();
	// mapa.fitMarkers(array); // not reloading map

  });
```

## install it
bower install manviny/mny_leaflet
