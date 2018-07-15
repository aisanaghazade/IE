<template>
    <div id = 'cart'>
        <header1></header1>
        <div id = "line">
            <div id = "section1">

            </div>
            <div id = "cartsection">
                <img src="../icons/cart-green.png" class="image">
            </div>
            <div id = "section2">

            </div>
            <div id = "sendsection">
                <img src="../icons/car-black.png" class="image">
            </div>

            
            <div id = "section3">

            </div>
            <div id = "paysection">
                <img src="../icons/payment-black.png" class="image">
            </div>
        </div>
        <div></div>
        <div id="headercolor"></div>
        <table2></table2>
        <footer1></footer1>
    </div>
</template>

<script>
import header1 from '@/components/header1';
import footer1 from '@/components/footer1';
import table2 from '@/components/table2';
export default {
    components: {
        header1, footer1, table2
    }
    
}
</script>

<style scoped>
@import "../pages/CSSFiles/general.css";
#cart{
    position: absolute;
    width: 1200px;
}

#line{
    border-style:  solid none none none;
    position: absolute;
    top: 200px;
    border-color: rgb(150, 150, 150);
    width: 1300px;
    height: 20px;
    border-width: 3px;
    float: right;

}

#section1{
    border-style:  solid none none none;
    position: absolute;
    top: -3px;
    border-color: rgb(0, 209, 139);
    width: 350px;
    height: 20px;
    border-width: 3px;
    float: right;
    right: 0px;

}
#cartsection{
    position: absolute;
    top: -3px;
    right: 350px;
    width: 120px;
    height: 60px;
    border-bottom-left-radius: 103px;  
    border-bottom-right-radius: 103px; 
    border: 3px solid rgb(0, 209, 139);
    border-top: 0;
    background-color: white;
}

#section2{
    border-style:  solid none none none;
    position: absolute;
    top: -3px;
    border-color: rgb(150, 150, 150);
    width: 150px;
    height: 20px;
    border-width: 3px;
    float: right;
    right: 470px;

}
#sendsection{
    position: absolute;
    top: -3px;
    right: 620px;
    width: 120px;
    height: 60px;
    border-bottom-left-radius: 103px;  
    border-bottom-right-radius: 103px; 
    border: 3px solid rgb(150, 150, 150);
    border-top: 0;
    background-color: white;
}

#section3{
    border-style:  solid none none none;
    position: absolute;
    top: -3px;
    border-color: rgb(150, 150, 150);
    width: 150px;
    height: 20px;
    border-width: 3px;
    float: right;
    right: 740px;

}
#paysection{
    position: absolute;
    top: -3px;
    right: 890px;
    width: 120px;
    height: 60px;
    border-bottom-left-radius: 103px;  
    border-bottom-right-radius: 103px; 
    border: 3px solid rgb(150, 150, 150);
    border-top: 0;
    background-color: white;
}


.image{
    position: relative;
    right: -40px;
}

#headercolor{
    position: absolute;
    top: 400px;
    width: 1300px;
    right: -100px;
    background-color: rgba(241,245,248);
    height: 35px;
}
</style>


