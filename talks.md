---
layout: default
title: Talks
permalink: /talks/
---

<div class="content-card">
  <h1>Talks</h1>

  <link rel="stylesheet" href="{{ '/leaflet/leaflet.css' | relative_url }}">
  <script src="{{ '/leaflet/leaflet.js' | relative_url }}"></script>

        <style>
          /* Map dimensions and style */
          #map { 
            height: 600px; 
            width: 100%; 
            border-radius: 4px; /* Slightly reduced to match standard card aesthetic */
            border: 1px solid #eee; 
            z-index: 1; /* Ensures map stays below certain navigation elements if necessary */
          }
        </style>    
        
        <div id="map"></div>

        <script>
        document.addEventListener("DOMContentLoaded", function () {
          var map = L.map('map').setView([20, 0], 2);
          L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
            attribution: '© OpenStreetMap contributors'
          }).addTo(map);

          const talks = [
            {
              title: "19th Panhellenic conference in mathematical analysis",
              venue: "National Technical University, Athens Greece",
              lat: 37.97849,
              lng: 23.785228
            }
          ];

          talks.forEach(t => {
            L.marker([t.lat, t.lng])
              .addTo(map)
              .bindPopup("<strong>" + t.title + "</strong><br>" + t.venue);
          });
        });
        </script>
</div>