<template>
    <div id = "row">
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
                <td class = "c31"></td>
                <td class = "c41"></td>
            </tr>
        </table>
    </div>
</template>

<script>
export default {
    props:[
        'item', 'brandname', 'name1', 'name2', 'name3', 'color', 'size', 'code', 'count', 'source'
    ],
    methods:{
        plus: function(){
            this.count++;
        },
        minus: function(){
            if (this.count > 1) {
                this.count--;
            }
        }
    }
}
</script>

<style scoped>

@import "../pages/CSSFiles/general.css";
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
    width: 335px;
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
    background-color: rgba(241,245,248);
}

</style>


