---
title: People
layout: splash
permalink: /people/
people:
  - title: "People"
    excerpt: "OHSU Computation consists of many groups, staff, faculty, and students. If you want to join, we want you! To add yourself, look at the [instructions in the README for this repository.](https://github.com/drylabyrinth/drylabyrinth.github.io/blob/master/README.md)"
---

<script
  src="https://code.jquery.com/jquery-3.3.1.min.js"
  integrity="sha256-FgpCb/KJQlLNfOu91ta32o/NMZxltwRo8QtmkMRdAu8="
  crossorigin="anonymous"></script>

<script src="https://unpkg.com/imagesloaded@4/imagesloaded.pkgd.min.js"></script>

<script src="https://unpkg.com/isotope-layout@3/dist/isotope.pkgd.min.js"></script>

{% include feature_row %}
{% include feature_row id= "people" type = "center" %}
{% assign sorted_people = site.people | sort: 'last_name' %}

## Filter by Group:

{% assign sorted_interests = site.data.research_interests | sort: 'name' %}
{% assign sorted_groups = site.data.groups | sort: 'name' %}

<div class="button-group filter-button-group">
	<a class="button active btn btn--info" data-filter="*">All</a>
	{% for tag in sorted_groups %}
		<a class="button btn btn--info" data-filter=".{{ tag.acronym }}">{{ tag.name }}</a>
	{% endfor %}
</div>

## Filter by research interest:

<div class="button-group filter-button-group">
	<a class="button active btn btn--info" data-filter="*">All</a>
	{% for tag in sorted_interests %}
		<a class="button btn btn--info" data-filter=".{{ tag.tag }}">{{ tag.name }}</a>
	{% endfor %}
</div>

<div class="grid__wrapper">
	{% for person in sorted_people %}
    {% include people.html %}
  {% endfor %}
</div>



<style type="text/css">

	a.button.active {
		background: #F76B48;
		color: #fff;
	}

body {
	height: 100%;
	cursor: default;
}

#card {
	float: left;
	width: 350px;
	height: 350px;
	margin: 10% auto;
	border-radius: 8px;
	box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.2), 0px 2px 6px rgba(0, 0, 0, 0.4);
}

#profile {
	cursor: grabbing;
	width: 350px;
	height: 350px;
	position: relative;
	top: 30px;
	border-radius: 8px;
}

img {
	width: 100px;
	height: 100px;
	border-radius: 100px;
	top: 32px;
	display: block;
	margin: 0 auto;
}

.card1 {
	color: rgba(38, 50, 56, 1);
	font-family: 'Roboto Condensed', sans-serif !important;
	font-size: 30px !important;
	font-weight: 700;
	text-align: center;
	position: relative;
	top: 20px;
}

.icons {
	text-align: center;
	position: relative;
	top: 15px;
}

.card2 {
	color: rgba(38, 50, 56, .87);
	font-family: 'Roboto Condensed', sans-serif !important;
	font-size: 14px !important;
	font-weight: 400;
	text-align: center;
	position: relative;
	top: 10px;
}
.card3 {
	color: rgba(38, 50, 56, .87);
	font-family: 'Roboto Condensed', sans-serif !important;
	font-size: 12px !important;
	font-weight: 400;
	text-align: center;
	position: relative;
	top: 10px;
}

</style>

<script>

	// init Isotope

	var $container = $(".grid__wrapper").imagesLoaded(function(){
		$container.isotope({
			layoutMode : 'fitRows',
			itemSelector: '.card'
	  		// options
		});
	});
  
	// filter items on button click
	$('.filter-button-group').on( 'click', 'a', function() {
	  var filterValue = $(this).attr('data-filter');
	  $container.isotope({ filter: filterValue });
	});

	$('.button-group a.button').on('click', function(){
		$('.button-group a.button').removeClass('active');
		$(this).addClass('active');
	});

</script>
