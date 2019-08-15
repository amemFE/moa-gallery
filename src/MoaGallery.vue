<template>
     <div class="inner-banner-outer pt-0" v-if="images != undefined && images.length > 0">
      <div class="col-12 img-main" v-if="images.length >= 5">
        <div class="row">
          <BlueMapGallery :images="images" :index="index" @close="index = null"></BlueMapGallery>
          <div
            @click="index = 0"
            class="col-6 p-0 img-left"
            :style="{ backgroundImage: 'url(' + images[0].href + ')' }"
          ></div>
          <div class="col-md-6 col-sm-12 p-0">
            <div class="row m-0">
              <div
                v-for="n in 4"
                :key="n"
                @click="index = n"
                class="col-md-6 col-sm-12 p-0 img-right"
                :style="{ backgroundImage: 'url(' + images[n].href + ')' }"
              ></div>
            </div>
          </div>
        </div>
      </div>

      <div class="p-0 col-12 img-main" v-else>
        <BlueMapGallery :images="images" :index="index" @close="index = null"></BlueMapGallery>
        <div
          @click="index = 0"
          class="img-left"
          :style="{ backgroundImage: 'url(' + images[0].href + ')' }"
        ></div>
      </div>
      <div class="col-12 text-right more-btn-main">
        <button @click="index = 0" class="btn more-btn">View Photos</button>
      </div>
    </div>
</template>

<script>
import BlueMapGallery from "./Gallery.vue"

  export default {
    name:'Gallery',
    props: {
      images: {
        type: Array,
        default() {
          return [];
        },
      },
    },

    data() {
      return {
       index: null
      };
    },
    components:{
      BlueMapGallery
    },

    methods: {
      }
  };
</script>



<style scoped>
 .img-right {
  opacity: 1;
  height: 350px;
  background-repeat: no-repeat;

  background-size: cover;
  background-position: center;
  transition: all 0.5s ease;
  border: solid 1px #000;
}
.img-left:hover,
.img-right:hover {
  /* transform: scale(1.2); */
  cursor: pointer;

  opacity: 0.8;
}
.img-left {
  height: 700px;
  opacity: 1;
  background-repeat: no-repeat;
  background-position: center;
  background-size: cover;
  border: solid 1px #000;
}

.img-sect {
  width: 100%;
  padding-top: 70px;
  padding-bottom: 50px;
  /* border-top: 4px solid rgba(0, 0, 0, 0.1); */
  border-top: 4px solid rgba(0, 166, 127, 0.2);
  /* padding-top: 155px; */
  float: left;
  width: 100%;
}
.img-main {
  background-color: #000;
}
.more-btn-main {
  position: relative;
  top: -83px;
  right: 20px;
}
.more-btn:hover {
  background: #00a59c;
  color: #fff;
}
.more-btn {
  padding: 10px 33px;
  /* border: solid 2px #eee; */
  background: #383838;
  color: #fff;
  font-weight: 900;
  font-size: 18px;
  text-transform: capitalize;
}


@media (max-width:768px) {
  .img-right{
    display: none;
  }
  .img-left{
    cursor: pointer;
    opacity: .8;
    height: 365px !important;
    max-width: 100%;
    flex: 0 0 100%;
    border: 0 !important;
}
}
</style>
 

