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
            <row v-for="r in rows" :key='r' v-bind:item="r.item" v-bind:brandname="r.brandname" v-bind:name1='r.name1' v-bind:name2='r.name2' v-bind:name3='r.name3' v-bind:color='r.color' v-bind:size='r.size' v-bind:code='r.code' v-bind:src='r.src' v-bind:count='r.count' v-bind:cost='r.cost' v-bind:discount='r.discount'></row>
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
                {item: 1, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 36, code:'123456', scr:"", count:1, discount:0.1, cost:10000},
                {item: 2, brandname: 'adidas', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 37, code:'123456', scr:"", count:1, discount:0.1, cost:10000},
                {item: 3, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 38, code:'123456', scr:"", count:1, discount:0.1, cost:10000},
                {item: 4, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 39, code:'123456', scr:"", count:1, discount:0.1, cost:10000},
                {item: 5, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 36, code:'123456', scr:"", count:1, discount:0.1, cost:10000},
                {item: 6, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 36, code:'123456', scr:"", count:1, discount:0.1, cost:10000},
                {item: 7, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 39, code:'123456', scr:"", count:1, discount:0.1, cost:10000},
                {item: 8, brandname: 'nike', name1: 'name', name2: 'name', name3: 'name', color: 'black', size: 40, code:'123456', scr:"", count:1, discount:0.1, cost:10000}
            ]
        }
    }
}
</script>

<style scoped>
@import "../pages/CSSFiles/general.css";
#rows{
    position:absolute;
    top: 34px;
    left: 5px;
    height:450px;
    overflow-y: scroll;
}
#table{
    position: absolute;
    top: 400px;
    right: 150px;
    width: 905px;
    float: right;
    /* border-style: solid; */
    direction: rtl;
    
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


