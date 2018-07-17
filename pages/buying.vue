<template>
    <div id = 'buying'>
        <cart v-if="a == 0"></cart>
        <sending v-if="a == 1"></sending>
        <payment v-if="a == 2"></payment>
        <button v-if="a != 2" id = "next"  @click = "plus()">ثبت و مرحله بعد</button>
    </div>
</template>

<script>
import cart from '@/components/cart'
import sending from '@/components/sending';
import payment from '@/components/payment';
export default {
    components:{
        cart,sending,payment
    },
    data(){
        return{
            a:0
        }
    },
    methods:{
        plus: function(){
            this.a++;
        }
    }
}
</script>

<style scoped>

@import "./CSSFiles/general.css";

#next{
    position: absolute;
    top: 970px;
    left: 200px;
    width: 200px;
    border-radius: 20px;
    border-style: none;
    background-color: rgb(37, 37, 224);
    color: white;
}
</style>


