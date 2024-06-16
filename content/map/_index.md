---
title: "土浦用水のページ"
---

<div id="map" style="height: 600px;"></div>

<script src="https://unpkg.com/leaflet/dist/leaflet.js"></script>
<script>
    // 地図を初期化
    var map = L.map('map').setView([35.682839, 139.759455], 13);
    
    // タイルレイヤーを追加
    L.tileLayer('https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '© OpenStreetMap contributors'
    }).addTo(map);

    // マーカーを追加
    var marker = L.marker([35.682839, 139.759455]).addTo(map);
    
    // ポップアップに画像と説明文を追加
    var popupContent = `
        <b>ここには何があるでしょう</b><br>
        <img src="./images/ichinoya_deguchi.jpg.jpg" alt="説明画像" style="width:100px;height:100px;"><br>
        簡単な説明はなんでしょう．
    `;
    marker.bindPopup(popupContent).openPopup();
</script>

