    <!doctype html>
    <html>
    <head>
    
    <!-- Adding in the Leaflet CSS file -->
    <link rel="stylesheet" href="http://cdn.leafletjs.com/leaflet-0.6.4/leaflet.css" />
    <!--[if lte IE 8]>
         <link rel="stylesheet" href="http://cdn.leafletjs.com/leaflet-0.6.4/leaflet.ie.css" />
    <![endif]-->

    <!-- Adding Leaflet JavaScript file -->
    <script src="http://cdn.leafletjs.com/leaflet-0.6.4/leaflet.js"></script>

    <!-- Adding styling info for the map -->
    <style type="text/css">
    #map { height: 600px; }
    </style>

    </head>

    <body>

      <!-- Creating the map div -->
      <div id="map"></div>

      <!-- The JavaScript that's powering the map -->
      <script>

      // Initialize the map
      var map = L.map('map').setView([45.51,-122.67], 14);

      // Add tiles
      L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
      }).addTo(map);

      // Add a marker
      var marker = L.marker([45.516469,-122.676208]).addTo(map);

      // Add a popup to the marker
      marker.bindPopup("EsriPDX");

      </script>
    </body>
    </html>