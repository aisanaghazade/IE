<template>
    <div id="row">
        <img src="../icons/runningshoe.jpg" id="item1">
        <img src="../icons/runningshoe.jpg" id="item2">
        <img src="../icons/runningshoe.jpg" id="item3">
        <img src="../icons/runningshoe.jpg" id="item4">
    </div>
</template>

<script>
export default {
    components:{
    },
    data () {
    return {
      items: [
          {brandname:'nike' ,name:'running' ,Pbefore:'100000' ,Pafter:'90000' ,N:'30' ,class:"item"},
          {brandname:'nike' ,name:'running' ,Pbefore:'100000' ,Pafter:'90000' ,N:'30' ,class:"item"},
          {brandname:'nike' ,name:'running' ,Pbefore:'100000' ,Pafter:'90000' ,N:'30' ,class:"item"},
          {brandname:'nike' ,name:'running' ,Pbefore:'100000' ,Pafter:'90000' ,N:'30' ,class:"item"},
          {brandname:'nike' ,name:'running' ,Pbefore:'100000' ,Pafter:'90000' ,N:'30' ,class:"item"},
          {brandname:'nike' ,name:'running' ,Pbefore:'100000' ,Pafter:'90000' ,N:'30' ,class:"item"}
      ]
    }
  }
}

</script>

<style scoped>
#row{
    position: absolute;
    top: -150px;
    width: 600px;
    height: 200px;
}

#item1{
    position: absolute;
    top: 120px;
    right: -50px;
    float: left;
    transform: rotate(-90deg);
    height: 140px;
    width: 140px;
}

#item2{
    position: absolute;
    top: 120px;
    right: 100px;
    float: left;
    transform: rotate(-90deg);
    height: 140px;
    width: 140px;
}

#item3{
    position: absolute;
    top: 120px;
    right: 250px;
    float: left;
    transform: rotate(-90deg);
    height: 140px;
    width: 140px;
}

#item4{
    position: absolute;
    top: 120px;
    right: 400px;
    float: left;
    transform: rotate(-90deg);
    height: 140px;
    width: 140px;
}
</style>
