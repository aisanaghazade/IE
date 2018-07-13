<template>
    <div id="slider">
    <b-carousel id="carousel1"
                controls
                background="#FFFFFF"
                :interval="4000"
                img-width="900"
                img-height="300"
                v-model="slide"
                @sliding-start="onSlideStart"
                @sliding-end="onSlideEnd"
    >
        <b-carousel-slide  img-blank img-alt="Blank image" >
            <div class="slide">
            <slide1></slide1>
            </div>
        </b-carousel-slide>

        <b-carousel-slide  img-blank img-alt="Blank image">
            <div class="slide">
            <slide1></slide1>
            </div>
        </b-carousel-slide>

    </b-carousel>


  </div>
</template>

<script>
import slide1 from '@/components/slide1';
export default {
    components:{
        slide1
    }
}
</script>

<style scoped>
#slider{
    position: absolute;
    transform: rotate(90deg);
    float: right;
    width: 850px;
    height: 350px;
    border-style: solid;
    border-width: 1px;
    border-color: rgb(255, 255, 255);
    right: -250px;
    top:230px;
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
    border-color: rgb(255, 255, 255);
}

.slide{
    position: relative;
    float: left;
    top: 0px;
    height: 150px;
    width: 800px;
}
</style>

