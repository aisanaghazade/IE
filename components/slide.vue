<template>
    <div id="row">
        <span id="item1"><item brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item></span>
        <span id="item2"><item brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item></span>
        <span id="item3"><item brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item></span>
        <span id="item4"><item brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item></span>
        <span id="item5"><item brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item></span>
    </div>
</template>

<script>
import item from '@/components/item'
export default {
    components:{
        item
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
    width: 800px;
    height: 200px;
}

#item1{
    position: absolute;
    top: 0px;
    right: -80px;
    float: left;
}

#item2{
    position: absolute;
    top: 0px;
    right: 90px;
    float: left;
}

#item3{
    position: absolute;
    top: 0px;
    right: 260px;
    float: left;
}

#item4{
    position: absolute;
    top: 0px;
    right: 430px;
    float: left;
}

#item5{
    position: absolute;
    top: 0px;
    right: 600px;
    float: left;
}
</style>
