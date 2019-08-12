vue-cover-gallery
==========

This is a vue 2 based modern gallery which can be used instead of a cover photo. First 5 images in the array will be displayed in the cover view; however, if the array has less than 5 images, first image will be displayed as the cover photo and other imgaes can be viewed by clicking on an image or invoking the 'View Photos' button.

This Gallery is a modification of [vue-Gallery](https://github.com/RobinCK/vue-gallery)


  <!-- * [Getting Started Guide](http://www.idangero.us/swiper/get-started/)
  * [API](http://www.idangero.us/swiper/api/)
  * [Demos](http://www.idangero.us/swiper/demos/)
  * [Forum](http://www.idangero.us/swiper/forum/) -->
  
![alt text](https://s3-us-west-2.amazonaws.com/moa-static-files/extra_images/Screenshot+from+2019-03-26+17-24-29.png)

## Example

[Live demo](https://test-project-2baad.firebaseapp.com/)


## Getting start

Install boostrap,jQuery and popper.js (ignore these 2 steps if you already have)

```
$ npm i bootstrap jquery popper.js
```
Import to your main.js

```
import 'bootstrap'; 
import 'bootstrap/dist/css/bootstrap.min.css';
```
After installing this dependencies
```
$ npm i vue-cover-gallery --save
```

Then imprort gallery to a vue component.

```html
import Gallery from "vue-cover-gallery"
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
import Gallery from "vue-cover-gallery"
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

* clone from Github.
* install dependencies.
 ```
 npm install
 ```
* For live testing excute below line from the root directory.

```
vue serve ./src/example/example.vue
```

* Do your modifications.
* Run a build 
```
npm run build
```
* You can use build files in dist folder

* You should install blueimp-gallery (dependency) exteranally for this case.

```
npm i blueimp-gallery --save
```
```html
import * as Gallery from "./gallery.umd.js (path to gallery.umd.js)"
```
* Then do all things, same as `Getting start` section.
