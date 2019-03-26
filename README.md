npm-moa-gallery
==========

This is a vue 2 based modern gallery which can be used instead of a cover photo. First 5 images in the array will be displayed in the cover view; however, if the array has less than 5 images, first image will be displayed as the cover photo and other imgaes can be viewed by clicking on an image or invoking the 'View Photos' button.

This Gallery is a modification of [vue-Gallery](https://github.com/RobinCK/vue-gallery)


  <!-- * [Getting Started Guide](http://www.idangero.us/swiper/get-started/)
  * [API](http://www.idangero.us/swiper/api/)
  * [Demos](http://www.idangero.us/swiper/demos/)
  * [Forum](http://www.idangero.us/swiper/forum/) -->


## Getting start
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
## Modifications/Build/Contribution

You can import directly from npm or clone from git hub modify and build.

[GitHub](https://github.com/amemFE/moa-gallery) repository.

1. clone from Github.
2. install dependencies.
 ```
 npm install
 ```
3. Do your modifications.
4. Run a build 
```
npm run build
```
5. you can use build files in dist folder

you should install blueimp-gallery (dependency) exteranally for this case.

```
npm i blueimp-gallery --save
```
```html
import Gallery from "./gallery.umd.js (path to gallery.umd.js)"
```
6. Then do all things, same as `Getting start` section.