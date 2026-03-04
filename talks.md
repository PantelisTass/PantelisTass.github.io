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
    #map { 
      height: 600px; 
      width: 100%; 
      border-radius: 4px; 
      border: 1px solid #eee; 
      z-index: 1; 
    }
    /* Style for the link inside the popup */
    .popup-link {
      display: inline-block;
      margin-top: 10px;
      color: #800020; /* Your Burgundy */
      font-weight: bold;
      text-decoration: none;
    }
    .popup-link:hover {
      text-decoration: underline;
    }
  </style>    
  
  <div id="map"></div>

  <script>
  document.addEventListener("DOMContentLoaded", function () {
    // 1. Initialize map (Centered on Europe)
    var map = L.map('map').setView([48.0, 15.0], 4);

    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
      attribution: '© OpenStreetMap contributors'
    }).addTo(map);

    // 2. Data Array
    const talks = [
      {
        title: "19th Panhellenic conference in mathematical analysis",
        venue: "National Technical University, Athens Greece",
        lat: 37.97849,
        lng: 23.785228,
        pdf: "/files/Brownian regularity Analysis conf greece 2025.pdf"
      }, 
      {
        title: "Cambridge probability seminar",
        venue: "DPMMS, Cambridge University, United Kingdom",
        lat: 52.2104,
        lng: 0.1030, 
        // Use a simple path string to avoid Liquid processing errors
        pdf: "/files/Brownian_Regularity_of_the_KPZ_fixed_point_Cambridge__slides.pdf"
      }
    ];

    // 3. Add Markers
    talks.forEach(function(t) {
      var content = "<strong>" + t.title + "</strong><br>" + t.venue;
      
      if (t.pdf) {
        content += "<br><a href='" + t.pdf + "' target='_blank' class='popup-link'>View Slides (PDF)</a>";
      }

      L.marker([t.lat, t.lng]).addTo(map).bindPopup(content);
    });
  });
  </script>
</div>