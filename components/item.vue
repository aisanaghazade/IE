<template>
    <div class="Item">
    <div class = "product-Item">
        <div class = "discount">
            <p class = "text5">N%</p>
        </div>
        <div class = "Image-of-item">
            <!-- <p class="text6"> Product Image</p> -->
            <img src="../icons/placeholder-image.png" class="Image1"/>
        </div>
    </div>
    <div class="item-informations">
        <p class = "text1">{{brandname}}</p>
        <p class = "text2">{{name}}</p>
        <p><span class = "text3">{{Pbefore}}</span><span class="text4">{{Pafter}}</span></p>
        <p class = "text7">تومان</p>
    </div>
    </div>
</template>

<script>
export default {
    props: ['brandname','address','name','Pbefore','Pafter']
}
</script>


<style scoped>
@import '../pages/CSSFiles/general.css';

.Item{
    display:block;
    direction: rtl;
}

.text1{
    float: right;
    font-size: 80%;
    margin-top: 13%;
    margin-right: -6%;
}

.text2{
    float: right;
    font-size: 90%;
    margin-top: 14.2%;
    margin-right: -7%;
    color: rgb(187, 182, 182);
}

.text3{
    float: right;
    font-size: 60%;
    margin-top: 15.8%;
    margin-right: -9.8%;
    color: rgb(0, 0, 0);
    text-decoration: line-through;
}

.text4{
    float: right;
    font-size: 60%;
    margin-top: 15.8%;
    margin-right: -3%;
    color: rgb(212, 10, 135);
}

.text7{
    float: right;
    font-size: 60%;
    margin-top: 17%;
    margin-right: -5.75%;
    color: rgb(212, 10, 135);
}

.product-Item{
    align-content: center;
    direction: rtl;
    border-style: solid;
    border-color: rgba(206, 206, 206, 0.952);
    width: 10%;
    height: 50%;
    float: right;
    margin-right: 2%;
    margin-top: 2%;

}

.text6{
    font-size: 120%;
    align-content: center;
    bottom: 40%;
    top: 20%;
    margin-right: 5%;
}



.discount{
    border-radius: 100%;
    margin-top: -15px;
    margin-right: -15px;
    width: 50px;
    height: 50px;
    border-style: solid;
    border-color: rgb(228, 74, 125);;
    background-color: rgb(228, 74, 125);

}

.text5{
    margin-top: 30%;
    margin-right: 30%;
}

.Image1{
    float: right;
    width: 180px;
    margin-right: -25%;
    margin-top: -30%

}


</style>


