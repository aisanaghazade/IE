<template>
    <div id="searchResult">
    <header1></header1>
    <div id = "classes">
        <button class="minimize">-</button>
        <h1 class="title"> 
            دسته‌بندی‌ها
        </h1>
        <div id="classification">
            <classes id="class"></classes>
        </div>
    </div>
    <div id = "brands">
        <button class="minimize1">-</button>
        <h1 class="title"> 
            براساس برند
        </h1>
        <input type="text" placeholder="جست‌وجوی برند" id="brandsearch">
        <div id="brandname">
            <brands></brands>
        </div>
    </div>
    <div id = "colors">
        <button class="minimize">-</button>
        <h1 class="title"> 
            رنگ
        </h1>
        <colorbox></colorbox>
    </div>
    <Result pagecount='1' pagenumber='3'></Result>
    <div id="footer">
        <footer1></footer1>
    </div>
    </div>
</template>
<script>

import footer1 from "@/components/footer1";
import header1 from "@/components/header1";
import classes from '@/components/classes';
import Result from '@/components/results';
import brands from '@/components/brands';
import colorbox from '@/components/colorbox';

export default {
    components:{
        header1, footer1, classes, Result, brands, colorbox
    },
    head: {
    // To use "this" in the component, it is necessary to return the object through a function
    title: {
        inner:'clouthster'
    },
    meta: [
      { name: 'viewport', content: 'width=device-width, initial-scale=1' }
    ],
    script:[
        {src:'https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js'},
        {src:'https://ajax.googleapis.com/ajax/libs/jquery/3.3.1/jquery.min.js'}
    ],
    link:[
        {rel:'stylesheet', href:'https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css'}
    ],
    
  }
}

</script>

<style scoped>

@import "./CSSFiles/general.css";
#searchResult{
    width: 1200px;
    position: absolute;
}

#footer{
    position: relative;
    top: 200px;
}

#classes{
    position: absolute;
    top:150px;
    right: 0px;
    background-color: rgba(241,245,248);
    width: 200px;
    direction: rtl;
    height: 250px;
    overflow-y: scroll;
}

#brands{
    position: absolute;
    top:430px;
    right: 0px;
    background-color: rgba(241,245,248);
    width: 200px;
    direction: rtl;
    height: 250px;
}

#colors{
    position: absolute;
    top:710px;
    right: 0px;
    background-color: rgba(241,245,248);
    width: 200px;
    direction: rtl;
    height: 250px;
}

.color{
    width: 20px;
    height: 20px;
    background-color: black;
    position: relative;
    top: 10px;
}
#colorbox{
    width: 180px;
    height: 240px;
    position: absolute;
    top: 100px;
}
#class{
    direction: rtl;
    position: absolute;
    right: 10px;
}

.title{
    position: absolute;
    float: right;
    top: 5px;
    right: 5px;
}
#classification{
    position: relative;
    right: 0px;
    top: 10px;
    overflow-y: scroll;
    overflow-x: scroll;
    height: 210px;
}
.minimize{
    border-style: none;
    background-color:rgba(241,245,248);
    font-size: 150%; 
    position: relative;
    height: 25px;
    padding: 0px;
    left: 15px;
    
}
.minimize1{
    border-style: none;
    background-color:rgba(241,245,248);
    font-size: 150%; 
    position: relative;
    height: 25px;
    padding: 0px;
    left: -150px;  
}


#brandname{
    position: absolute;
    top: 60px;
    overflow-y: scroll;
    overflow-x: scroll;
    height: 170px;
    width: 190px;
}

#brandsearch{
    position: relative;
    top: 25px;
    left: 15px;
}


</style>

