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
  var parameters = {
    gridContainer: '#grid-container',
    gridItems: '.grid-item',
    enableImagesLoaded: false
  };
  var grid = new justifiedGrid(parameters);
  grid.initGrid();
</script>
```

### Customizing
Most of the customizing work will be done directly in the CSS, here is the commented version

```css
#grid-container { // The grid container
  width: 90%; // well, the width, obviously
  margin: auto; // just in order to center it
  overflow: hidden; // important, it allows this div to actually have a height since grid items are in float:left;
}

.grid-item {
  opacity: 0; // for the animation, you can remove it.
  float: left; // important
  padding: 5px; // the gutter
  box-sizing: border-box; // so that the gutter works well
}

.grid-item img { // just in case you want to wrap the image inside a link for example
  width: 100%;
  height: 100%;
}

.grid-item.loaded { // the loaded animation
  opacity: 1;
  transition: opacity .5s;
}
```

### Options
- **gridContainer** : your grid container selector
- **gridItems** : your grid items selector
- **enableImagesLoaded** : (*optional*)(*default: false*) determine if justified should use the awesome plugin from Dessandro "ImagesLoaded" ( you'll have to include it yourself though ).

### MIT License
Justified is released under the MIT License. Have fun with it.

### Credits
- **Demo Pictures** : they are all from pixabay :) thanks to their awesome users sharing these super cool pictures !
- **ImagesLoaded** : another awesome jquery plugin from Dessandro. Check his website : https://github.com/desandro/imagesloaded