<template>
    <div id = "profile">
        <header1></header1>
        <div id = "user">
            <h1 id="text1">{{user.name}}</h1>
            <div>
            <label class = "text2">نام و نام خانوادگی<br>
                <input type="text" placeholder="برای مثال آیسان آقازاده" class="input">
            </label>
            </div>
            <div>
            <label class = "text2">شماره تلفن همراه<br>
                <input type="tel" placeholder="برای مثال ۰۹۱۹۶۷۷۴۲۸۰" class="input">
            </label>
            </div>
            <div>
            <label class = "text3"><br>تاریخ تولد
                <datepicker id = "date" :language="fa"></datepicker>
            </label>
            </div>
            <div>
            <label class = "text5">رمز عبور فعلی<br>
                <input type="text" class="input">
            </label>
            <label class = "text4">رمز عبور جدید<br>
                <input type="text" class="input">
            </label>
            <label class = "text7">تکرار رمز عبور <br>
                <input type="text" class="input">
            </label>
            </div>
            <img v-bind:src="user.src" id = "image">
            <form id = "gender">
            <input type="radio" name="gender" value="female"> زن
            <input type="radio" name="gender" value="male"> مرد
            </form>
            <div>
            <label class = "text6">شهر<br>
                <input type="text" placeholder="برای مثال تهران" class="input">
            </label>
            </div>
            <div>
            <label class = "text6">شماره تلفن ثابت<br>
                <input type="tel" placeholder="برای مثال ۰۲۱۲۲۱۹۱۴۸۳" class="input">
            </label>
            </div>
            <div>
            <label class = "text6">شماره کارت ۱۶ رقمی<br>
                <input type="tel"  class="input"></input>
            </label>
            </div>
        </div>
        <button id=change>ثبت تغییرات</button>
        <div id = "a">
        <div id="address"> 
            <span id="a1"> <h1> آدرس‌ها</h1></span>
            <span ><button id="a2" @click="showaddress()">+</button></span>
            <div v-if="address == true">
            <div id="bailees">
            <div class = "bailees" v-for="b in bailees" :key="b" >
            <!-- <input type="radio" v-if="b.c == 1"> -->
                <detailsail v-bind:c='b.c' v-bind:address='b.address' v-bind:bailee='b.bailee' v-bind:homenumber='b.homenumber' v-bind:phonenumber='b.phonenumber' v-bind:postalcode='b.postalcode'></detailsail>
            </div>
            </div>
            <button id = "newaddress">اضافه کردن آدرس جدید</button>
            </div>
            <div>

            </div>
        </div>
        <div id="orders"> 
            <span id="a1"> <h1> سفارشات</h1></span>
            <span ><button id="a3" @click="showorders()">+</button></span>
            
            <div>
                
            </div>
        </div>
        </div>
        <div id="footer"><footer1></footer1></div>
        
    </div>
</template>

<script>
import Datepicker from 'vuejs-datepicker';
import header1 from '@/components/header1';
import detailsail from '@/components/detailsail';
import footer1 from '@/components/footer1';
export default {
    components:{
        header1, footer1, Datepicker,detailsail
    },
    data: function(){
        return{
            user:{name: 'aisan aghazade', src:""},
            address:false,
            orders:false,
            bailees:[
                {c:1, index:0, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:1, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:2, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:3, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:4, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:5, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'}
            ]
            
        }
    },
    methods:{
        showaddress: function(){
            if (this.address) {
                this.address = false;
            }else{
                this.address = true;
            }
        },
        showorders: function(){
            if (this.orders) {
                this.orders = false;
            }else{
                this.orders = true;
            }
        }
    }
    
}
</script>

<style scoped>
@import "./CSSFiles/general.css";
#a{
    position: absolute;
    top: 740px;
    right: 100px;
}
#newaddress{
    position: relative;
    top: 200px;
    right: 350px;;
    width: 200px;
    border-radius: 20px;
    border-style: none;
    background-color: rgb(37, 37, 224);
    color: white;
}
#change{
    width: 200px;
    position: relative;
    border-style: none;
    border-color: rgb(200, 200, 200);
    background-color: rgb(49, 49, 206);
    color: white;
    border-radius: 20px;
    top: 627px;
    right: -550px;
}
#footer{
    position: absolute;
    bottom: -500px;
}
#bailees{
    position: absolute;
    top: 30px;
    width: 1200px;
    right: -150px;
    height: 160px;
    overflow-y: scroll;
}

#profile{
    position: absolute;
    width: 1200px;
}
#a1{
    float: right;
}
#a2{
    border-style: none;
    background-color: white;
}
#a3{
    border-style: none;
    background-color: white;
}
#address{
    position: relative;
    top: 0px;
    right: 0px;
}
#orders{
    position: relative;
    top: 240px;
    right: 0px;
}
.text6{
    text-align: right;
    position: relative;
    right: -50px;
    margin-top: 30px;
    top: -550px;
    color:rgb(0, 0, 200);
}
#gender{
    position: relative;
    top:-280px;
    right: -405px;
}
#image{
    width: 180px;
    height: 180px;
    border-radius: 183px;
    border-style: solid;
    position: relative;
    top: -300px;
    left: 350px;
}
#date{
    position: relative;
    right: 0px;
    width: 200px;
}
#user{
    position: absolute;
    top: 200px;
    width: 900px;
    border-style: solid;
    border-color: rgb(167, 167, 167);
    border-width: 1px;
    right: 100px;
    height: 500px;
    direction: rtl;
}
#text1{
    position: relative;
    top: 25px;
    text-align: center;
    font-size: 200%;
    color: rgb(167, 167, 167);
    margin-bottom: 10px;
}
.text2{
    text-align: right;
    position: relative;
    right: -650px;
    margin-top: 30px;
    color:rgb(0, 0, 200);
}
.text5{
    text-align: right;
    position: relative;
    right: -250px;
    margin-top: 30px;
    color:rgb(0, 0, 200);
}
.text7{
    text-align: right;
    position: relative;
    right: -50px;
    margin-top: 30px;
    color:rgb(0, 0, 200);
}
.text3{
    text-align: right;
    position: relative;
    right: -680px;
    margin-top: 30px;
    color:rgb(0, 0, 200);
}

.text4{
    text-align: right;
    position: relative;
    right: -150px;
    margin-top: 30px;
    color:rgb(0, 0, 200);
}

.input{
    border-radius: 20px;
    margin-top: 5px;
    border-style: solid;
    border-width: 1px;
    width: 200px;
    border-color: rgb(200, 200, 200);
    background-color:  rgba(241,245,248);;
}
</style>


