<template>
    <tr v-for="(item) in rows" :key='item'>
                <td class= "c11">
                    <span class="img"><img class="image" src=""></span>
                    <span class="info">
                        <p class="text1">{{item.brandname}}</p>
                        <p class = "text2">{{item.name1}} {{item.name2}} {{item.name3}}</p>
                        <p class="text2">رنگ:{{item.color}}</p>
                        <p class="text2">سایز:{{item.size}}</p>
                        <p class="text2">کد کالا:{{item.code}}</p>
                    </span>
                </td>
                <td class = "c21">
                    <span><button id="plus" @click = "plus(item)">+</button></span>
                    <span id="count"> {{item.count}} </span>
                    <span><button id="plus" @click = "minus(item)">-</button></span>
                    
                </td>
                <td class = "c31"></td>
                <td class = "c41"></td>
            </tr>
</template>

<script>
  export default {
    
  }
</script>

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





        <template>
    <div id = "table">
        <table id = 'table1'>
            <tr>
                <th class = 'c1' id = 'r1c1'>مشخصات محصول</th>
                <th class = 'c2' id = 'r1c2'>تعداد</th>
                <th class = 'c3' id = 'r1c3'>قیمت</th>
                <th class = 'c4' id = 'r1c4'></th>
            </tr>
        </table>
        <div id = "rows">
            <row v-for="r in rows" :key='r' ></row>
        </div>
    </div>
</template>

<script>
import row from '@/components/row';
export default {
    components:{
        row
    },
    data(){
        return{
            a:1,
            rows:[
                {item: 1, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 36, code:'123456', scr:"", count:1},
                {item: 2, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 36, code:'123456', scr:"", count:1}
            ]
        }
    }
}
</script>

<style scoped>
@import "../pages/CSSFiles/general.css";
#rows{
    position:absolute
}
#table{
    position: absolute;
    top: 400px;
    right: 150px;
    width: 903px;
    float: right;
    /* border-style: solid; */
    direction: rtl;
    height: 450px;
    overflow-y: scroll;
}

#table1{
    position: relative;
    top: 0px;
    right: 0px;
    width: 900px;
    border-style: solid;
    border-width: 0px;
    float: right;
    border-style: solid;
    direction: rtl;
}

.c1{
    width: 330px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: none;
}

.c2{
    width: 210px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: none;
}

.c3{
    width: 330px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: none;
}

.c4{
    width: 40px;
    direction: rtl;
    text-align: center;
    border-color: rgb(190, 190, 190);
    border-right-style: solid;
    border-left-style: solid;
    border-bottom-style: solid;
}

#r1c1{
    background-color: rgba(241,245,248);
    border-top-style: none;
    border-bottom-style: none;
    height: 35px;
}
#r1c2{
    background-color: rgba(241,245,248);
    border-top-style: none;
    border-bottom-style: none;
}
#r1c3{
    background-color: rgba(241,245,248);
    border-top-style: none;
    border-bottom-style: none;
}
#r1c4{
    background-color: rgba(241,245,248);
    border-top-style: none;
    border-bottom-style: none;
}


</style>


