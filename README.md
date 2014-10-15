##How to create a new angular component (bower)
[Brian Ford](http://briantford.com/blog/angular-bower)  

# How to use it

1. bower install manviny/mny_leaflet --save 
2. check that all js and css libraries are loaded
3. inject 'manviny.mny-leaflet' into your app module
4. add  mnymapa to your controller
5. start using it


mny_leaflet example
===================

```javascript
angular
  .module('myApp', [
...
    'ngRoute',
    'manviny.mny-leaflet',
    ... ])
```


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


```html
<div class="center" ng-controller="LocalizaCtrl">
    <leaflet center="centerHere" markers="myMarkers"  layers="layers" defaults="defaults"  ></leaflet>
</div>
````
