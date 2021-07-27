#  map 출력하기

> 출력하는 경우 , `div` 태그로 출력
>
> ```html
> <div id="map"></div>
> ```





## 1. Google Map

> [ 구글의 지도 API 관련 URL ](https://developers.google.com/maps/gmp-get-started?hl=ko)

### 0. 구글 지도 API 키 값 입력하기

```html
<script src="https://maps.googleapis.com/maps/api/js?key=키값" ></script>
```



####  javascript 소스

### 1-1. 특정 위도, 경도를 입력하여 출력하는 경우

```html
<script>
    var dom = document.getElementById("map");
    if(dom) {
        new google.maps.Map(dom, {
            center: { lat: 37.5096357, lng: 127.0555218},
            zoom: 16
        });
    }     
</script>
```





### 1-2. marker를 찍어서 출력하는 경우

```html
<script>
    var dom = document.getElementById("map");
    if(dom) {
        var latlng = { lat: 37.5096357, lng: 127.0555218}
        var map = new google.maps.Map(dom, {
            center: latlng,
            zoom: 16
        });
        new google.maps.Marker({position: latlng, map: map})
    }     
</script>
```





### 1-3. 주소를 입력받아 지도를 출력하는 경우

```html
<script>
	var dom;
	var addr;
	function inputaddress() {
		addr = window.prompt("주소를 입력하세요");
		var url= 'https://maps.googleapis.com/maps/api/geocode/json?key=AIzaSyDy81EbO46BRSnX1DOgg_F84bhsdbku2z4&address='
							+ encodeURIComponent(addr)
					
	   	var request = new XMLHttpRequest();
		request.onload = function(event) {
			if (request.status == 200) {
				var obj = JSON.parse(request.responseText);
				lat = obj.results[0].geometry.location.lat;
				lng = obj.results[0].geometry.location.lng;
				dom.innerHTML = '';
				googlemap(lat, lng);
			}
		};
		request.open('GET', url, true);
		request.send();
	}
	
	function googlemap(latp, lngp) {
		var latlng = { lat: latp, lng: lngp }
		var map = new google.maps.Map(dom, {
	       	center: latlng,
	       	zoom: 16
	   	});
			    
	    var image = {
			  url: '../../images/duke.png',
			  size: new google.maps.Size(50, 60),
			  origin: new google.maps.Point(0, 0),
			  anchor: new google.maps.Point(17, 34),
			  scaledSize: new google.maps.Size(25, 25)
		};
						
		var marker = new google.maps.Marker({position: latlng, icon : image, map: map});

		var contentString =
				       "<h2 style='color:red;'>" + addr + "<br>("+lat+":"+lng+")</h2>";
						
		var infowindow = new google.maps.InfoWindow({
		    content: contentString
		});
						
		marker.addListener('click', function() {
		    infowindow.open(map, marker);
		});
	}


	window.onload = function () {
		dom = document.getElementById('map');
		document.getElementById('btn').onclick = inputaddress;
	}
</script>
```
