---
layout: page
title: travel
permalink: /travel/
order: 3
---

<div id="body">
  <div id="main">
  	
  	  {% for trip in site.data.travel %}
	  	  <div class="travel">
			  {% for photo in trip.photos %}

			      <img src="{{ photo }}" width="400px" height="300px" >
			      <h1 class="text">{{ trip.title }}</h1>

			  {% endfor %}
		  </div>
	  {% endfor %}

  </div>
</div>

<script type="text/javascript">
    var index=0;
    function flipPhotos(){ 
      [].forEach.call(document.images,function (v,i) { document.images[i].hidden = i!==index;});
      index = (index+1) % document.images.length;
    }
    window.onload = function () {setInterval(flipPhotos, 1000),hideTd("travel")};

    
    function hideTd(className){
	    var elements = document.getElementsByClassName(className);
	    for(var i = 0, length = elements.length; i < length; i++) {      
	       elements[i].style.display = 'block'; 
	    }
 	}
 </script>