<!DOCTYPE html>
<html lang="en">
<head>
<link rel="stylesheet" href="styles.css">
<Title>Homegrown Aeroponics</title>
</head>
<body>
<!--heading of page-->
<div>
<img src="badabong.png" style="width:5%;position: absolute;margin-left:800;">
<h1>Homegrown Aeroponics</h1>
<h2>Become Dependable</h2>
</div>
<!--heading of page-->

<!--Menu Bar-->
<div class="ButtonDiv">
	<button class="button button1" onclick="window.location.href='MainPage.html';">Home</button>
	<button class="button button1" onclick="window.location.href='News.html';">News</button>
	<button class="button button1" onclick="window.location.href='products.html';">Products</button>
	<button class="button button1" onclick="window.location.href='About-Us.html';">About Us</button>
	<button class="button button1" onclick="window.location.href='Profile.html';">Profile</button>
	<button class="button button1">Settings?</button>
</div>
<!--Menu Bar-->

<!-- images-->
<div class="ImgGallery">
	<div Class="Images fadeout"> 
		<img src="test1.png" class="CapCon">
		<div class="CaptionText">test 1</div>
	</div>
	<div Class="Images fadeout">
		<img src="test2.png" class="CapCon">
		<div class="CaptionText">This is test 2</div>
	</div>
	<div Class="Images fadeout">
		<img src="bop.jpg" class="CapCon">
		<div class="CaptionText">A random image for testing</div>
	</div>
	
	<div class="row">
		<div class="column">
			<img class="Thumbnail cursor" src="test1.png" style="width:80%" onclick="currentSlide(1)">
		</div>
		<div class="column">
			<img class="Thumbnail cursor" src="test2.png" style="width:100%" onclick="currentSlide(2)">
		</div>
		<div class="column">
			<img class="Thumbnail cursor" src="bop.jpg" style="width:100%" onclick="currentSlide(3)">
		</div>
	</div>
</div>




<div class="maintext">
<p>This is the Main Page</p>
<p>Will have an overview of the product and whatever else is wanted here.</p>
<p></p>
</div>
<script>
var slideIndex = 1;
showSlides(slideIndex);

function plusSlides(n) {
  showSlides(slideIndex += n);
}

function currentSlide(n) {
  showSlides(slideIndex = n);
}
function showSlides(n) {
  var i;
  var slides = document.getElementsByClassName("Images");
  var dots = document.getElementsByClassName("dot");
  if (n > slides.length) {slideIndex = 1}
  if (n < 1) {slideIndex = slides.length}
  for (i = 0; i < slides.length; i++) {
      slides[i].style.display = "none";
  }
  for (i = 0; i < dots.length; i++) {
      dots[i].className = dots[i].className.replace(" active", "");
  }
  slides[slideIndex-1].style.display = "block";
    dots[slideIndex-1].className += " active";
} 
</script>
</body>
</html>
