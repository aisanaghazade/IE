<template>
    <div v-if="a==1" id = "row">
        <table>
            <tr>
                <td class= "c11">
                    <span class="img"><img class="image" src=""></span>
                    <span class="info">
                        <p class="text1">{{brandname}}</p>
                        <p class = "text2">{{name1}} {{name2}} {{name3}}</p>
                        <p class="text2">رنگ:{{color}}</p>
                        <p class="text2">سایز:{{size}}</p>
                        <p class="text2">کد کالا:{{code}}</p>
                    </span>
                </td>
                <td class = "c21">
                    <span><button id="plus" @click = "plus()">+</button></span>
                    <span id="count"> {{count}} </span>
                    <span><button id="plus" @click = "minus()">-</button></span>
                    
                </td>
                <td class = "c31">
                    <div id = "part1">
                        <p>
                            <span id = "span1">قیمت واحد</span>
                            <spna id = "span2">{{cost}} تومان</spna>
                        </p>
                        <p>
                            <span id = "span3">تخفیف </span>
                            <spna id = "span4">{{c}} تومان </spna>
                        </p>
                        <p>
                            <span id = "span5">قیمت نهایی </span>
                            <spna id = "span6">{{d}} تومان </spna>
                        </p>
                    </div>
                </td>
                <td class = "c41">
                    <button id="delete" @click = "del()"><img id="image1" src="../icons/delete.png"></button>
                </td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    props:[
        'item', 'brandname', 'name1', 'name2', 'name3', 'color', 'size', 'code', 'count', 'source','cost','discount'
    ],
    methods:{
        plus: function(){
            this.count++;
        },
        minus: function(){
            if (this.count > 1) {
                this.count--;
            }
        },
        del: function(){
            this.a--;
        }
    },
    computed:{
        c: function() {
            return (this.cost*this.dicount);
        },
        d: function(){
            return (this.cost - this.c);
        }
    },
    data(){
        return{
            a:1
        }
    }
}
</script>

<style scoped>

@import "../pages/CSSFiles/general.css";
#part1{
    position: relative;
    direction: rtl;
    width: 90%;
    height: 30px;
    margin-right: 5%;
    border-bottom-style: solid;
    border-bottom-width: 1px;
}
#span1{
    text-align: right;
    direction: rtl;
    right: 0px;
    /* border-style: solid; */
    position: relative;
    right: -80px;
    top: -30px;
}
#span2{
    text-align: left;
    direction: rtl;
    /* border-style: solid; */
    position: relative;
    right: 40px;
    top: -40px;
}

#span3{
    text-align: right;
    direction: rtl;
    right: 0px;
    /* border-style: solid; */
    position: relative;
    right: -90px;
    top: -40px;
    color: rgb(255,0,100);
}
#span4{
    text-align: left;
    direction: rtl;
    /* border-style: solid; */
    position: relative;
    right: 40px;
    top: -40px;
    color: rgb(255,0,100);
}

#span5{
    text-align: right;
    direction: rtl;
    right: 0px;
    /* border-style: solid; */
    position: relative;
    right: -80px;
    top: -20px;
}
#span6{
    text-align: left;
    direction: rtl;
    /* border-style: solid; */
    position: relative;
    right: 40px;
    top: -20px;
}

#image1{
    width: 10px;
    height: 10px;
}
#delete{
    width: 15px;
    height: 15px;
    background-color: rgba(241,245,248);
    border-style: none;
}
#plus{
    border-radius: 100%;
    border-style: none;
    width: 30px;
    height: 30px;
    font-size: 140%;
    color: rgb(238, 238, 238);
    background-color: rgb(88, 88, 88);
}
#count{
    margin-right: 5px;
    margin-left: 5px;
    color: rgb(88, 88, 88);
}
.image{
    width: 80px;
    height: 110px;
}
.info{
    float: right;
    direction: rtl;
    margin-right: 10px;
    margin-top: 5px;
}
.img{
    position: relative;
    float: right;
    margin-right: 10px;
}
.text1{
    direction: rtl;
    text-align: right;
    color: rgb(194, 191, 191);
    font-size: 120%;
    margin-bottom: 0.5px;
}
.text2{
    direction: rtl;
    text-align: right;
    color: rgb(75, 75, 75);
    font-size: 100%;
    margin-bottom: 0.5px;
}

.c11{
    width: 332.5px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: none;
    height: 150px;
    border-bottom-style: solid;
}


.c21{
    width: 212px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: none;
    height: 150px;
    border-bottom-style: solid;
}


.c31{
    width: 332.5px;
    right: 3px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: none;
    height: 150px;
    border-bottom-style: solid;
}


.c41{
    width: 40.5px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: solid;
    height: 150px;
    border-bottom-style: solid;
    border-top-style: solid;
    border-top-width: 0.2px;
    background-color: rgba(241,245,248);
}

</style>


