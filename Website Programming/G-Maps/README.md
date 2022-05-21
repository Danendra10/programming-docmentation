# GOOGLE MAPS API

If you wanna use google maps on ur web, u can use this line

```
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY&callback=myMap"></script>
```

make the div line in ur html

```
<div id="map" style="width:100%;height:400px;"></div>
```

it's all up to you how you would like to style it

after having that div component and script set up, we want to get the data from the g-maps api to load on our id which "map"

```
<script>
function myMap() {
var mapProp= {
  center:new google.maps.LatLng(51.508742,-0.120850),
  zoom:5,
};
var map = new google.maps.Map(document.getElementById("map"),mapProp);
}
</script>
```

we defined the map properties on "mapProp" variable, and loaded it in google.maps.Map function

you can go to [this link](https://developers.google.com/maps/documentation/javascript/get-api-key) to learn how to get your g-maps api, it should looks like this
```
<script src="https://maps.googleapis.com/maps/api/js?key=YOUR_KEY&callback=myMap"></script>
```

## Adding marker

you can define a marker using this function
```
google.maps.Marker
```

so it would look like
```
var marker = new google.maps.Marker({position: myCenter});

marker.setMap(map);
```

the setMap parameter takes the name of the map that you defined before, which is "map"

### Creating your marker animations

#### Bouncing animations
you can do this by adding "animation:google.maps.Animation.BOUNCE" in your Marker functiion
```
var marker = new google.maps.Marker({
  position:myCenter,
  animation:google.maps.Animation.BOUNCE
});

marker.setMap(map);
```