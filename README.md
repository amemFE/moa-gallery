npm-moa-Gallery
==========

This is a vue 2 based modern gallery, which can be used as a cover. First 5 images in the array will be displayed as a cover view, If the array has less than 5 images first image will be shown as cover. Other images can be seen by clicking on an image or clicking view photos button.

This Gallery is a modification of [vue-Gallery](https://github.com/RobinCK/vue-gallery)

# Getting Started
  <!-- * [Getting Started Guide](http://www.idangero.us/swiper/get-started/)
  * [API](http://www.idangero.us/swiper/api/)
  * [Demos](http://www.idangero.us/swiper/demos/)
  * [Forum](http://www.idangero.us/swiper/forum/) -->

### Installation/usage

### Getting start
```
$ npm i npm-moa-gallery --save
```

Then imprort gallery to a vue component.

```html
import Gallery from "npm-moa-gallery"
```

Then include Gallery as a child component

```html
components: {
    Gallery
  },
```

Include the the Gallery in HTML divition (give image array as an Input)

```html
<Gallery :images="images" ></Gallery>
```

Structure of the image array (href is required other 2 fields optional)

```html
[{
            title: "",
            description: "",
            href: ""
 }]
```

## Example Vue-2 component

```html
<template>
  <Gallery :images="images" ></Gallery>
</template>
  
<script>
import Gallery from "npm-moa-gallery"
export default {
  
  name: "Example",
  components: {
    Gallery
  },
  data() {
    return {
      images: [
            {
            title: "title 1",
            description: "des 1",
            href: "https://www.exapleimages.com/first.jpg"},
            {
             title: "title 2",
            description: "des 2",
            href: "https://www.exapleimages.com/second.jpg"
            },
     ],
    };
  },
};
</script>

<style scoped>

</style>
```
