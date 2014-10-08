---
layout: post
title: "Instagram photos map"
description: ""
category: 
- gis
- photography
- hows to
tags: []
---
{% include JB/setup %}

I have been using instagram for several months. Since all photos I upload are taken with my phone, all of them have location coordinates. In fact, instagram has a cool feature to show them on a map.

The problem is that the map is only available from the mobile app and it can not be shared with other users through the web, or at least I did not find the way. So, I started to find a way to show a map with my instagram photos.

Luckyly there is a [plugin for Leaflet](https://github.com/turban/Leaflet.Instagram) to show instagram photos using this great javascript library. The only problem is that [instagram API](http://instagram.com/developer/endpoints/) lets get only the last 20 photos from a user by default, but the endpoint allows to pass it the number of media elements to return, and by means of another endpoint we can know the number of media elements by user.

The code below gets all your instagram photos and show them on a map with [OpenStreetMap](http://openstreetmap.org) as base layer, you only need your instagram user id and a developer token.

    <div id="map"></div>
        <script src="http://code.jquery.com/jquery-2.1.0.min.js"></script>
        <script src="./Leaflet.Instagram/examples/lib/fancybox/jquery.fancybox.pack.js"></script>       
        <script src="./Leaflet.Instagram/examples/lib/reqwest.min.js"></script>
        <script src="./Leaflet.Instagram/examples/lib/leaflet/leaflet.js"></script>
        <script src="./Leaflet.Instagram/examples/lib/cluster/leaflet.markercluster.js"></script>           
        <script src="./Leaflet.Instagram/dist/Leaflet.Instagram.Fancybox.Cluster.js"></script>      
        <script>
     
        var map = L.map('map').setView([40.47, -3.75], 5);
     
        L.tileLayer('http://{s}.tile.osm.org/{z}/{x}/{y}.png', {
            attribution: '&copy; <a href="http://osm.org/copyright">OpenStreetMap</a> contributors'
        }).addTo(map);
     
        $.ajax({
            type: "GET",
            dataType: "jsonp",
            cache: false,
            url: "https://api.instagram.com/v1/users/YOUR_USER_ID_HERE?access_token=YOUR_INSTAGRAM_TOKEN_HERE",
            success: function (data) {
                var url = 'https://api.instagram.com/v1/users/YOUR_USER_ID_HERE/media/recent?access_token=YOUR_INSTAGRAM_TOKEN_HERE&count=' + data.data.counts.media;
                L.instagram.cluster(url, {
                featureGroup: L.instagram.fancybox
                }
                ).addTo(map);
            }
        });
        </script>

You can see as it looks like in the [About page](http://psanxiao.com/about.html) of this blog.

