<template>
  <div>
    <div v-for="b in brands" :key="b" class="brand">
        <span class = "name">
            {{b.en}}
        </span>
        <span>
            <input type="checkbox" class = "checkbox" >
            <span class = "brandname">{{b.fa}}</span>
        </span>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      brands: [
        {en: "nike", fa:"نایک"},
        {en: "puma", fa:"پوما"},
        {en: "adidas", fa:"آدیداس"},
        {en: "kafsh melli", fa:"کفش ملی"},
        {en: "nike", fa:"نایک"},
        {en: "puma", fa:"پوما"},
        {en: "adidas", fa:"آدیداس"},
        {en: "kafsh melli", fa:"کفش ملی"}
      ]
    }
  }
}

</script>

<style scoped>
.brand{
    border-style: none none solid none;
    border-color: rgb(192, 192, 192);
    border-width: 0.05px;
    height: 30px;
    width: 180px;
    position: relative;
    right: 10px;
    
}
.checkbox{
    border-radius: 0%;
    border-style: solid;
    float: right;
    position: relative;
    top: 5px;
    right: -15px;
    width: 35px;
}

.brandname{
    direction: rtl;
    float: right;
    position: relative;
    top: 5px;
    right: -10px;
}

.name{
    float: left;
    position: relative;
    top:5px;

}
</style>
