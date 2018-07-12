<template>
    <div id="searchResult">
    <header1></header1>
    <div id = "classes">
        <classes id="class"></classes>
    </div>
    <footer1></footer1>
    </div>
</template>
<script>

import item from '@/components/item'
import footer1 from "@/components/footer1";
import header1 from "@/components/header1";
import classes from '@/components/classes'

export default {
    components:{
        item, header1, footer1, classes
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
    ]
  }
}

</script>

<style scoped>

@import "./CSSFiles/general.css";
#searchResult{
    width: 1200px;
    position: absolute;
}

#classes{
    position: absolute;
    top:150px;
    right: 0px;
    background-color: rgba(241,245,248);
    width: 250px;
    direction: rtl;
    height: 300px;
}

#class{
    direction: rtl;
    position: absolute;
    top: 10px;
    right: 10px;
}

</style>

