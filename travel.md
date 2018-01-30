---
layout: page
title: travel
permalink: /travel/
order: 3
---

<div id="body">
  <div id="main">
  	
	  	  <div class="travel" style="height: 290px;">

			  {% for trip in site.data.travel %}

			      <img src="{{ trip.photo }}" width="400px" height="300px" style="border-radius: 4px;" >
			     

			  {% endfor %}
		  </div>
	

  </div>
</div>

<script type="text/javascript">
    var index = 0;

    function flipPhotos(){ 
      [].forEach.call(document.images,function (v,i) { document.images[i].hidden = i!==index;});
      index = (index+1) % document.images.length;
    }

    window.onload = function () {
 
    	setInterval(flipPhotos, 1000),hideTd("travel")};

    
    function hideTd(className){
	    var elements = document.getElementsByClassName(className);

	    //elements[1].style.display = 'none'; 
	    console.log("length",elements.length);
	    for(var i = 0, length = elements.length; i < length; i++) {
	      
	       elements[i].style.display = 'block'; 
	    }
 	}
 </script>