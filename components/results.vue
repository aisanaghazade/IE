<template>
    <div id="Result">
        <h3 id= "text1">
             نام دسته
        </h3>
        <h3 id="text2">
            مرتب‌سازی
        </h3>
        <b-form-select v-model="selected" :options="options" class="mb-3" />
        <button id="preP" disabled='true'>صفحه قبل</button>
        <span id="text3">
        صفحه{{pagecount}} از {{pagenumber}}
        </span>
        <button id="nextP">صفحه بعد</button>
        <div id = "items">
            <item v-for="i in items" :key="i" brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item>
            <item v-for="i in items" :key="i" brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item>
            <item v-for="i in items" :key="i" brandname='nike' name='running' Pbefore='100000' Pafter='90000' N='30' class="item"></item>
        </div>
        

    </div>
</template>

<script>
import item from '@/components/item'
export default {
    components:{
        item
    },
    props:[
        'pagecount', 'pagenumber'
    ],
  data () {
    return {
      selected: null,
      options: [
        { value: null, text: 'انتخاب کنید' },
        { value: 'a', text: 'محبوب‌ترین' },
        { value: 'b', text: 'گران‌ترین' },
        { value: {'C': '3PO'}, text: 'ارزان‌ترین' },
        { value: 'd', text: 'پرفروش‌ترین', disabled: true }
      ],
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

#Result{
    position: absolute;
    top: 150px;
    right: 230px;
    color: rgb(75, 75, 75);
    width: 900px;
    direction: rtl;
    height: 1000px;
}
#text1{
    position: absolute;
    right: 0px;
    font-size: 120%;
    direction: rtl;
}
#text2{
    position: absolute;
    right: 0px;
    font-size: 120%;
    top: 23px;
    direction: rtl;
    color: rgb(184, 184, 184)
}
.mb-3{
    width: 95px;
    float: right;
    height: 10px;
    position: absolute;
    top: 13px;
    right: 90px;
    border-radius: 0px;
    border-color: rgb(197, 197, 197);
    background-color: rgba(241,245,248);
    font-size: 80%;
}

#preP{
    border-radius: 0px;
    border-color: rgb(197, 197, 197);
    background-color: rgba(241,245,248);
    border-style: solid;
    border-width: 1px;
    position: relative;
    right: -120px;
    top: 13px;
    height: 36px;
    width: 80px;
}

#nextP{
    border-radius: 0px;
    border-color: rgb(197, 197, 197);
    background-color: rgba(241,245,248);
    border-style: solid;
    border-width: 1px;
    position: relative;
    right: -110px;
    top: 13px;
    height: 36px;
    width: 80px;
}
#text3{
    position: relative;
    right: -120px;
    top: 13px;
    height: 36px;
}
#items{
    position: absolute;
    top: 0px;
    width: 900px;
}
.item{
    position: relative;
    top: 0px;
    float: right;
}

</style>



