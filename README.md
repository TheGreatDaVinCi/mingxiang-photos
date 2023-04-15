# mingxiang-photos

```html
<script>
    function myFunction(imgs) {
  // Get the expanded image
  var expandImg = document.getElementById("expandedImg");
  // Get the image text
  var imgText = document.getElementById("imgtext");
  // Use the same src in the expanded image as the image being clicked on from the grid
  expandImg.src = imgs.src;
  // Use the value of the alt attribute of the clickable image as text inside the expanded image
  imgText.innerHTML = imgs.alt;
  // Show the container element (hidden with CSS)
  expandImg.parentElement.style.display = "block";
}
</script>
<style>
    /* The grid: Four equal columns that floats next to each other */
.column {
  float: left;
  width: 25%;
  padding: 10px;
}

/* Style the images inside the grid */
.column img {
  opacity: 0.8;
  cursor: pointer;
}

.column img:hover {
  opacity: 1;
}

/* Clear floats after the columns */
.row:after {
  content: "";
  display: table;
  clear: both;
}

/* The expanding image container (positioning is needed to position the close button and the text) */
.container {
  position: relative;
  display: none;
}

/* Expanding image text */
#imgtext {
  position: absolute;
  bottom: 15px;
  left: 15px;
  color: white;
  font-size: 20px;
}

/* Closable button inside the image */
.closebtn {
  position: absolute;
  top: 10px;
  right: 15px;
  color: white;
  font-size: 35px;
  cursor: pointer;
}
</style>
<!-- The grid: four columns -->
<div class="row">
  <div class="column">
    <img src="https://raw.githubusercontent.com/TheGreatDaVinCi/mingxiang-photos/master/3%E5%B0%BA%E7%83%A4%E6%BC%86%E6%91%BA%E7%96%8A%E7%8B%97%E7%B1%A0/IMG_20141219_170034.jpg" alt="P1" onclick="myFunction(this);">
  </div>
  <div class="column">
    <img src="https://raw.githubusercontent.com/TheGreatDaVinCi/mingxiang-photos/master/3%E5%B0%BA%E7%83%A4%E6%BC%86%E6%91%BA%E7%96%8A%E7%8B%97%E7%B1%A0/IMG_20141219_170137.jpg" alt="P2" onclick="myFunction(this);">
  </div>
  <div class="column">
    <img src="https://raw.githubusercontent.com/TheGreatDaVinCi/mingxiang-photos/master/3%E5%B0%BA%E7%83%A4%E6%BC%86%E6%91%BA%E7%96%8A%E7%8B%97%E7%B1%A0/IMG_20141219_170247.jpg" alt="P3" onclick="myFunction(this);">
  </div>
</div>

<!-- The expanding image container -->
<div class="container">
  <!-- Close the image -->
  <span onclick="this.parentElement.style.display='none'" class="closebtn">&times;</span>

  <!-- Expanded image -->
  <img id="expandedImg" style="width:100%">

  <!-- Image text -->
  <div id="imgtext"></div>
</div>
```
```html
<video width="320" height="240" controls>
  <source src="https://ocnxcloud.mooo.com/index.php/s/oJbW53nnHQYXA5C/download/Nextcloud%20intro.mp4" type="video/mp4">
  Your browser does not support the video tag.
</video>
```