<template>
    <div id="details">
        <header1></header1>
        <multipictureslider></multipictureslider>
        <Product></Product>
        <productinfo></productinfo>
        <multiItemSlider></multiItemSlider>
        <footer1></footer1>
    </div>
</template>

<script>
import multiItemSlider from '@/components/multiItemSlider';
import multipictureslider from '@/components/multipictureslider';
import footer1 from "@/components/footer1";
import header1 from "@/components/header1";
import Product from "@/components/Product";
import productinfo from "@/components/productinfo";
export default {
    components:{
        multiItemSlider, multipictureslider, header1, footer1, Product, productinfo
    }
}
</script>

<style scoped>
@import "./CSSFiles/general.css";
#details{
    width: 1200px;
    position: absolute;
}

</style>

