<template>
   <div id="slider">
    <b-carousel id="carousel1"
                controls
                background="#F1F5F8"
                :interval="4000"
                img-width="900"
                img-height="300"
                v-model="slide"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
    >

      
        <b-carousel-slide  img-blank img-alt="Blank image" >
            <div class="slide">
            <slide></slide>
            </div>
        </b-carousel-slide>

        <b-carousel-slide  img-blank img-alt="Blank image">
            <div class="slide">
            <slide></slide>
            </div>
        </b-carousel-slide>

    </b-carousel>


  </div>
</template>

<script>
import slide from '@/components/slide'
export default {
    components:{
        slide
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
  }
}
</script>

<style scoped>
#slider{
    position: absolute;
    float: right;
    width: 1500px;
    height: 300px;
    border-style: solid;
    border-width: 1px;
    border-color: rgb(255, 255, 255);
    right: -300px;
    background-color: rgba(241,245,248);
    top:1220px;
    padding-left: 100px;
}
#carousel1{
    position: relative;
    float: right;
    height: 300px;
    width: 1100px;
    right: 300px;
    top:0px;
    border-color: rgb(255, 255, 255);
}

.slide{
    position: relative;
    float: left;
    top: -70px;
    height: 150px;
    width: 1000px;
    right: 50px;
}
</style>

