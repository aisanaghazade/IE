<template>
    <div class="homepage">
      <header1></header1>
      <div id="slider">
        <b-carousel id="carousel1"
                    style="text-shadow: 1px 1px 2px #333;"
                    controls
                    indicators
                    background="#ababab"
                    :interval="4000"
                    img-width="900"
                    img-height="300"
                    v-model="slide"
                    @sliding-start="onSlideStart"
                    @sliding-end="onSlideEnd"
        >


          <b-carousel-slide v-for='b in banners' :key="b" caption="product image" img-blank img-alt="Blank image">
            <img v-bind:src="b.bannerURL" v-bind:alt="b.bannerLink">
          </b-carousel-slide>


        </b-carousel>


      </div>
      <div id="cat1"><category name="مردانه"></category></div>
      <div id="cat2"><category name="زنانه"></category></div>

      <div id="cat3"><category name="بچه‌گانه"></category></div>
      <news></news>
      <footer1></footer1>

    </div>
</template>


<script>
import footer1 from "@/components/footer1";
import news from "@/components/news";
import header1 from "@/components/header1";
import slider from "@/components/slider";
import category from "@/components/category";
import axios from 'axios';
export default {
  components: {
    footer1,
    header1,
    slider,
    category,
    news
  },
  data () {
    return {
      slide: 0,
      sliding: null
    }
  },
  methods: {
    onSlideStart (slide) {
      this.sliding = true
    },
    onSlideEnd (slide) {
      this.sliding = false
    }
  },
  asyncData () {
    return axios.get('http://localhost:8003/homepagebanners')
  .then((res) => {
      return {banners: res.data.banners}

    })
  },
  head: {
    // To use "this" in the component, it is necessary to return the object through a function
    title: {
      inner: "clouthster"
    },
    meta: [
      { name: "viewport", content: "width=device-width, initial-scale=1" }
    ],
    script: [
      {
        src:
          "https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js"
      },
      {
        src: "https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js"
      }
    ],
    link: [
      {
        rel: "stylesheet",
        href:
          "https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css"
      }
    ]
  }
};
</script>

<style scoped>
@import "./CSSFiles/general.css";
.homepage{
    position: absolute;
    width: 1200px;
}

#cat3{
  position: absolute;
  top: 500px;
  right: 700px;
}

#cat2{
  position: absolute;
  top: 500px;
  right: 450px;
}

#cat1{
  position: absolute;
  top: 500px;
  right: 200px;
}
#slider{
  position: absolute;
  float: right;
  width: 950px;
  height: 350px;
  border-style: solid;
  border-width: 1px;
  border-color: rgb(231, 222, 222);
  right: 100px;
  top:140px;
  padding-left: 100px;
}
#carousel1{
  position: absolute;
  float: right;
  height: 300px;
  width: 900px;
  right: 00px;
  left: 25px;
  top:25px;
  border-color: rgb(228, 228, 228);
}
</style>
