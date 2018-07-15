<template>
    <div id="details">
        <header1></header1>
        <multipictureslider></multipictureslider>
        <Product></Product>
        <productinfo></productinfo>
        <div id= "tabs">
            <b-tabs id = "tabs1">
                <b-tab title="مشخصات محصولات" active id = "tab1"> 
                    <div> 
                        <b-table striped hover :items="items" id="table"></b-table>
                    </div>
                </b-tab>
                <b-tab title="نظرات کاربران" id = "tab2">
                    <div>

                    </div>
                </b-tab>
            </b-tabs>
        </div>
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

const items = [
  { مشخصه: 'a', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'b', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'ab', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'abc', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'abcd', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'b', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'ab', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'abc', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'abcd', مقدارمشخصه: 'salam masalan' },
  { مشخصه: 'abcde', مقدارمشخصه: 'salam masalan' }
]

export default {
    components:{
        multiItemSlider, multipictureslider, header1, footer1, Product, productinfo
    },
    data () {
    return {
      items: items
    }
    }
}
</script>

<style scoped>
@import "./CSSFiles/general.css";
#details{
    width: 1200px;
    position: absolute;
}

#tabs{
    position: absolute;
    top: 850px;
    width: 900px;
    right: 100px;
}

#nazarat{
    position: absolute;
    top: 1000px;
    width: 900px;
    border-style: solid;

}

#tab1{
    position: relative;
    top: 0px;
    width: 1000px;
    right: 0px;
    height: 300px;
    overflow-y: scroll;
    overflow-x: scroll;
}

#table{
    direction: rtl;
    position: absolute;
    right: 100px;
    text-align: center;
}

</style>

