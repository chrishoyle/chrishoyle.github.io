---
layout: page
title: travel
permalink: /travel/
order: 3
---

<div id="body">
  <div id="main">
  	<div id="pull-right" >
  	  {% for trip in site.data.travel %}
	  	  <div id="travel">
			  {% for photo in trip.photos %}

			      <img src="{{ photo }}" width="400px" height="300px" >
			      <h1 class="text">
			      {{ trip.title }}
			      </h1>
			  {% endfor %}
		  </div>
	  {% endfor %}
	</div>
  </div>
</div>

<script type="text/javascript">
    var index=0;
    function flipPhotos(){ 
      [].forEach.call(document.images,function (v,i) { document.images[i].hidden = i!==index;});
      index = (index+1) % document.images.length;
    }
    window.onload = function () {setInterval(flipPhotos, 1000)};
    document.getElementById("travel").style.display='block';
 </script>