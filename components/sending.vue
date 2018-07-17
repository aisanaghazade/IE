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
                <img src="../icons/car-green.png" class="image">
            </div>
            
            <div id = "section3">

            </div>
            <div id = "paysection">
                <img src="../icons/payment-black.png" class="image">
            </div>
        </div>
        <div id="bailees">
        <div class = "bailees" v-for="b in bailees" :key="b" >
            <!-- <input type="radio" v-if="b.c == 1"> -->
            <detailsail v-bind:c='b.c' v-bind:address='b.address' v-bind:bailee='b.bailee' v-bind:homenumber='b.homenumber' v-bind:phonenumber='b.phonenumber' v-bind:postalcode='b.postalcode'></detailsail>
            </div>
        </div>
        <button id = "newaddress">اضافه کردن آدرس جدید</button>
        <h5 id="time">زمان دریافت سفارش</h5>
        <b-form-select v-model="selected" :options="options" id="time-select" />
        <footer1></footer1>
        
    </div>
</template>

<script>
import header1 from '@/components/header1';
import footer1 from '@/components/footer1';
import detailsail from '@/components/detailsail';
export default {
    components: {
        header1, detailsail, footer1
    },
    data: function(){
        return{
            bailees:[
                {c:1, index:0, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:1, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:2, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:3, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:4, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'},
                {c:1, index:5, address:'ازگل نوبهار جنوبی نبش سبلان', bailee:'آیسان آقازاده', homenumber:'02122191483', phonenumber:'09196774280', postalcode:'postalcode'}
            ],
            selected: null,
            options:[
                { value: null, text: 'انتخاب کنید'},
                { value: 'a', text: '1'},
                { value: 'b', text: '2'},
                { value: 'c', text: '3'},
                { value: 'd', text: '4'}
            ]
        }
    },
    methods:{
        del: function (i) {
            for (let index = 0; index < this.bailees.length; index++) {
                if (this.bailees[index] == i) {
                    this.bailees[index].c--;
                }
                
            }
        }
    }
    
}
</script>

<style scoped>
@import "../pages/CSSFiles/general.css";
#time{
    position: absolute;
    top:800px;
    right: 100px;
}
#time-select{
    position: absolute;
    top: 850px;
    right: 100px;
    width: 300px;
    border-radius: 0px;
    border-color: rgb(197, 197, 197);
    background-color: rgba(241,245,248);
    font-size: 80%;

}
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
#delete{
    position: relative;
    margin-bottom:70px;
    right: -90px;
}
#newaddress{
    position: absolute;
    top: 750px;
    left: 200px;
    width: 200px;
    border-radius: 20px;
    border-style: none;
    background-color: rgb(37, 37, 224);
    color: white;
}
#bailees{
    position: absolute;
    top: 400px;
    width: 1200px;
    right: -50px;
    height: 300px;
    overflow-y: scroll;
}

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
    border-color: rgb(0, 209, 139);
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
    border: 3px solid rgb(0, 209, 139);
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
</style>


