
<html>
<style>
button {
width: 200;
height: 100;
background-color: #009900;
font-size: 20px;
color: white;
text-align:center;
border-radius: 12px;
font_family:"Engravers MT"
}
 </style>

<button onclick="getLocation()">SHARE LOCATION WITH FIRST RESPONDERS</button>
<p id="demo"></p>
<script>
var x = document.getElementById("demo");
function logError(error) {
    console.log(error);
}
function getLocation() {
  if (navigator.geolocation) {
    console.log("About to get location");
    navigator.geolocation.getCurrentPosition(showPosition, logError);
    console.log("Got location");
  } else { 
    console.log("Will not get location");
    x.innerHTML = "Geolocation is not supported by this browser.";
  }
}
function showPosition(position) {
  console.log("About to display location");
  x.innerHTML = "Latitude: " + position.coords.latitude + 
  "<br>Longitude: " + position.coords.longitude;
}
</script>

<button onclick="window.location='https://www.google.com/maps/place/Ann+Arbor,+MI/@42.2732991,-83.8077299,12z/data=!3m1!4b1!4m5!3m4!1s0x883cb00dd4431f33:0xdb09f94686c8b5e2!8m2!3d42.2808256!4d-83.7430378';">Map Navigation</button>


<title> </title>

<body> </body>
</html> 