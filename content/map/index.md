---
title: "土浦用水のページ"
---

<div id="map" style="height: 600px;"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
    var map = L.map('map').setView([35.682839, 139.759455], 13);
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '© OpenStreetMap contributors'
    }).addTo(map);

    var marker = L.marker([35.682839, 139.759455]).addTo(map);
    
    var popupContent = `
        <b>ここには何があるでしょう</b><br>
        <img src="./images/ichinoya_deguchi.jpg.jpg" alt="hoge" style="width:100px;height:100px;"><br>
        簡単な説明はなんでしょう．
    `;
    marker.bindPopup(popupContent).openPopup();
</script>

