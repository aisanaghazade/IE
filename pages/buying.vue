<template>
    <div id = 'buying'>
        <cart v-if="a == 0"></cart>
        <sending v-if="a == 1"></sending>
        <payment v-if="a == 2"></payment>
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
    }
}
</script>

<style scoped>

@import "./CSSFiles/general.css";
</style>


