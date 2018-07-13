<template>
    <div id= "productinfo">
        <h3 id="text1"> نام برند</h3>
        <div id="name">
            <span id="text2">نام محصول </span>
            <span id="text3">نام محصول </span>
            <span id = "text4">نام محصول </span>
        </div>
        <div id="price">
            <span id="before">قیمت قبل تخفیف</span>
            <span id="after">قیمت بعد تخفیف</span>
        </div>
        <div id='color1'>
            <span id='color'>رنگ:</span>
            <span id='color2'> نام رنگ</span>
        </div>
        <div id = 'pictures'>
            <span id='img1'><img src="" class="image"></span>
            <span id='img2'><img src="" class="image"></span>
            <span id='img3'><img src="" class="image"></span>
        </div>
        <div id='size'>
            <span>
                <b-form-select v-model="selected" :options="options" class="mb-3" />
            </span>
            <span id='link'>
                <a href="#" id="text5">راهنمای انتخاب سایز</a>
            </span>
        </div>
        <img src="../icons/hearticon.png" id="hearticon">
        <button id='add'>
            افزودن به سبد خرید
            <img src="../icons/cart.png" id='cartimage'>
        </button>
        
    </div>
</template>

<script>
export default {
    props:['brandname','name1','name2','name3','pbefore','pafter','color'],
    data () {
    return {
      selected: null,
      options: [
        { value: null, text: 'انتخاب کنید'},
        { value: 'a', text: '36'},
        { value: 'b', text: '37'},
        { value: 'c', text: '38'},
        { value: 'd', text: '39'}
      ]
    }}
}
</script>

<style scoped>
#productinfo{
    position: relative;
    top: 150px;
    right: -360px;

}

#text2{
    position: relative;
    right: 80px;
    direction: rtl;
    color: rgb(167, 167, 167);
}

#text3{
    position: relative;
    right: 100px;
    direction: rtl;
    color: rgb(167, 167, 167);
}

#text4{
    position: relative;
    right: 120px;
    direction: rtl;
    color: rgb(167, 167, 167);
}

#name{
    position: relative;
    right: 20px;
    top: 10px;
}

#price{
    position: relative;
    right: 100px;
    top: 20px;
}

#before{
    position: relative;
    direction: rtl;
    color: rgb(73, 73, 73);
    text-decoration: line-through;
}

#after{
    position: relative;
    right: 50px;
    direction: rtl;
    color: rgb(255, 16, 128);
}

#color{
    direction: rtl;
    position: relative;
    top: 30px;
    right: -15px;
    font-size: 110%;
}

#color1{
    direction: rtl;
    position: absolute;
}

#color2{
    direction: rtl;
    position: relative;
    top: 30px;
    right: -15px;
    font-size: 110%;
    width: 90px;
}
.image{
    width: 140px;
    height: 140px;
}

#img1{
    position: relative;
    top: 80px;
    right: 330px
}

#img2{
    position: relative;
    top: 80px;
    right: 320px
}

#img3{
    position: relative;
    top: 80px;
    right: 310px
}

.mb-3{
    width: 95px;
    float: right;
    height: 10px;
    position: relative;
    top: 30px;
    right: 100px;
    border-radius: 0px;
    border-color: rgb(197, 197, 197);
    background-color: rgba(241,245,248);
    font-size: 80%;
}

#size{
    position: relative;
    top: 80px;
    float: left;
    right: 0px;
}

#link{
    position: relative;
    top: 40px;
    right: 120px;
    color: rgb(134, 134, 134);
}

#text5{
    color: rgb(134, 134, 134);
}

#text5:hover{
    color: rgb(134, 134, 134);
    text-decoration: none;
}

#add{
    color: white;
    background-color: rgb(255, 16, 128);
    width: 180px;
    text-align: center;
    border-style: none;
    position: absolute;
    top: 460px;
    right: 1100px;
}

#cartimage{
    width: 10px;
    height: 10px;
}

#hearticon{
    position: relative;
    top: 180px;
    right: 320px;
    height: 25px;
}

</style>


