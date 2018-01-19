# Owl Carousel 2 Thumbnails plugin (Fixed Thumbs Owl Slider)
Enables thumbnail support for Owl Carousel 2.2.1

##### Added carousel for thumbs  

## Quick start
1) initialize owl carousel;
2) initialize thumbs carousel.

Screenshot:

![Alt text](https://monosnap.com/file/Xc4DypbDAGEB6zTUgSrcS3co5mj5jQ.png "Screenshot")

Example: 
```javascript
// initialize owl carousel

$(window).on('load', function () {
  var $owlThumbs = $('.owl-thumbs');
  if($owlThumbs.length && $owlThumbs.find('button').length > 1) {
    $owlThumbs.owlCarousel({
      autoplay: false,
      loop: true,
      nav: true,
      navText: [' ', ' '],
      dots: false,
      items: 7,
      margin: 0,
      thumbs: false,
      thumbImage: false,
      loadedClass: 'owl-carousel owl-loaded',
      responsive : {
          0 : {
              items : 3
          },
          380 : {
              items : 4
          },
          480 : {
              items : 5
          },
          590 : {
              items : 6
          },
          640 : {
              items : 7
          },
          768 : {
              items : 3
          },
          880 : {
              items : 4
          },
          992 : {
              items : 7
          }
      }
    });
  }
});
```

##### Enable thumbs
```javascript
$(document).ready(function(){
  $('.owl-carousel').owlCarousel({
    thumbs: true
  });
});
```

## Use pre-rendered html as thumbnails. **_recommended_**
```javascript
$(document).ready(function(){
  $('.owl-carousel').owlCarousel({
    thumbs: true,
    thumbsPrerendered: true
  });
});
```

##### Add thumbnails (link slider and thumbnails with data-slider-id attribute)
```html
<div class="owl-carousel" data-slider-id="1">
    <div>Your Content</div>
    <div>Your Content</div>
    <div>Your Content</div>
    <div>Your Content</div>
</div>
<div class="owl-thumbs" data-slider-id="1">
    <button class="owl-thumb-item">slide 1</button>
    <button class="owl-thumb-item">slide 2</button>
    <button class="owl-thumb-item">slide 3</button>
    <button class="owl-thumb-item">slide 4</button>
</div>
```

## Or add data-thumb attribute to your slides
```html
<div class="owl-carousel">
    <div data-thumb='Content of your thumbnail (can be anything)'> Your Content </div>
    <div data-thumb='Content of your thumbnail (can be anything)'> Your Content </div>
    <div data-thumb='Content of your thumbnail (can be anything)'> Your Content </div>
    <div data-thumb='Content of your thumbnail (can be anything)'> Your Content </div>
</div>
```

#### [demo](http://gijsroge.github.io/owl-carousel2-thumbs)

## Available options
```javascript
$(document).ready(function(){
  $('.owl-carousel').owlCarousel({
    // Enable thumbnails
    thumbs: true,
  
    // When only using images in your slide (like the demo) use this option to dynamicly create thumbnails without using the attribute data-thumb.
    thumbImage: false,

    // Enable this if you have pre-rendered thumbnails in your html instead of letting this plugin generate them. This is recommended as it will prevent FOUC
    thumbsPrerendered: true,
    
    // Class that will be used on the thumbnail container
    thumbContainerClass: 'owl-thumbs',
    
    // Class that will be used on the thumbnail item's
    thumbItemClass: 'owl-thumb-item'
  });
});
```
