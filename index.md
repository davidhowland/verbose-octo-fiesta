---
title: Home
layout: home
---
Cape Cod Trail Running is a guide to running and biking on the extensive trail networks of Cape Cod. Most people don't think of the Cape when they think of a place to go trail running or mountain biking but we have more than 1000 miles of trails covering all types of terrain and landscapes.

<div id='map' style='margin-top: 16px; width: 100%; height: 500px;'></div>

<script>
    mapboxgl.accessToken = 'pk.eyJ1IjoiY2FwZWNvZHRyYWlscnVubmluZyIsImEiOiJjbHgwc3pldGcwNDV6MmpxN3JtY3RjZTdhIn0.Xh5g0TNKifNbui-Nk2btGw';
    const map = new mapboxgl.Map({
        container: 'map', 
        style: 'mapbox://styles/capecodtrailrunning/clwjdfr1y02q901qlcu0u4i5i',
        center: [-70.355, 41.65], 
        zoom: 8.15, 
    });

    const nav = new mapboxgl.NavigationControl({
        showCompass: false
    });

    map.addControl(nav);

    {% for trailhead in site.trailheads %}
        const marker1 = new mapboxgl.Marker({ color: 'black'})
            .setLngLat([{{ trailhead.lat }}, {{ trailhead.lng }}])
            .addTo(map);
    {% endfor %}
</script>

Use the map above to browse trailheads and view a list of routes for each trailhead. The menu bar has a list of trailheads by town. Below is a table of routes that you can sort by distance.