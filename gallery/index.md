---
layout: page
title:  Gallery
excerpt: "A bundle of pictures"
comments: false
images:
 - image_path: /gallery/albums/alb01.jpg
   gallery-folder: /gallery/gallery01/
   gallery-name: Gallery1--厦门大学
   gallery-date: July 2015
 - image_path: /gallery/albums/alb02.jpg
   gallery-folder: /gallery/gallery02/
   gallery-name: gallery2
   gallery-date: June 2015
 - image_path: /gallery/albums/alb03.jpg
   gallery-folder: /gallery/gallery03/
   gallery-name: gallery3
   gallery-date: May 2015
 - image_path: /gallery/albums/alb04.jpg
   gallery-folder: /gallery/gallery04/
   gallery-name: gallery4
   gallery-date: April 2015
 - image_path: /gallery/albums/alb05.jpg
   gallery-folder: /gallery/gallery05/
   gallery-name: gallery5
   gallery-date: March 2015
 - image_path: /gallery/albums/alb06.jpg
   gallery-folder: /gallery/gallery06/
   gallery-name: gallery6
   gallery-date: February 2015
 - image_path: /gallery/albums/alb07.jpg
   gallery-folder: /gallery/gallery07/
   gallery-name: gallery7
   gallery-date: January 2015
 - image_path: /gallery/albums/alb08.jpg
   gallery-folder: /gallery/gallery08/
   gallery-name: gallery8
   gallery-date: December 2014
 - image_path: /gallery/albums/alb09.jpg
   gallery-folder: /gallery/gallery09/
   gallery-name: gallery9
   gallery-date: November 2014
---
<figure class= "3" >
    {% for image in page.images %}
    <figcaption>
    <h3 style="color=#987cb9">{{image.gallery-name}}</h3>
    <p>{{image.gallery-date}}</p>
    </figcaption>
    <a href="{{ site.url }}{{ site.baseurl }}{{ image.gallery-folder }}">
    <img src="{{ site.url }}{{ site.baseurl }}{{ image.image_path }}">
    </a>
    <br>
    <hr style="FILTER: progid:DXImageTransform.Microsoft.Shadow(color:#987cb9,direction:145,strength:35); width=80%; color=#987cb9; SIZE=5">

      {% endfor %}
</figure>
<!--


<div class="gallery masonry-gallery">

{% for image in page.images %}  	

	               <figure class="gallery-item">
                         <figure class="effect-selena">
					<header class='gallery-icon'>

<a href="{{ site.url }}{{ site.baseurl }}{{ image.gallery-folder }}">
<img src="{{ site.url }}{{ site.baseurl }}{{ image.image_path }}"></a>

					</header>
					<figcaption class='gallery-caption'>
						<div class="entry-summary">
							<h3>{{image.gallery-name}}</h3>
							<p>{{image.gallery-date}}</p>
						</div>
					</figcaption>
                       </figure>
				</figure>

{% endfor %}		

			</div>
            -->
