<template>
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

      
      <b-carousel-slide caption="product image 1" img-blank img-alt="Blank image">
        
      </b-carousel-slide>

       <b-carousel-slide caption="product image 2" img-blank img-alt="Blank image">
        
      </b-carousel-slide>

    </b-carousel>


  </div>
</template>

<script>
export default {
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
