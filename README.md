# justified
A jQuery plugin to create simple justified grids.

### Getting Started
Include the justified.js file and the justified.css file.

```html
<!-- In the header, after your own css -->
<link href="css/justified.css" rel="stylesheet">
```

```html
<!-- Just before closing body tag -->
<script src="js/justified.js"></script>
```

Let's now write the HTML

```html
<div id="grid-container">
  <img class="grid-item" src="images/tokyo-night.jpg">
  <img class="grid-item" src="images/tokyo-tower.jpg">
  <img class="grid-item" src="images/tokyo-view.jpg">
  <img class="grid-item" src="images/akihabara.jpg">
  <img class="grid-item" src="images/fuji.jpg">
  <img class="grid-item" src="images/lake-fuji.jpg">
</div>
```

You can now initialize the grid according to the html 

```html
<script>
  var grid = new justifiedGrid($('#grid-container'), $('.grid-item'));
  grid.initGrid();
</script>
```

### ImagesLoaded compatibility
You can allow justified grid to work with the jQuery plugin imagesLoaded by Dessandro this way :

```html
<script>
  var grid = new justifiedGrid($('#grid-container'), $('.grid-item'), true);
  grid.initGrid();
</script>
```