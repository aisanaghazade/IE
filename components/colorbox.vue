<template>
    <div id = "colorbox">
        <button v-for="color in colors" :key="color.id" :style="{background: color.color}" class="color">
</button>
    </div>
</template>

<script>
export default {
    data(){
        return{
            colors:[
                {id:'1', color:'#FFFF00'},
                {id:'1', color:'#FF007F'},
                {id:'1', color:'#00FF00'},
                {id:'1', color:'#CC99FF'},
                {id:'1', color:'#FF0000'},
                {id:'1', color:'#00FFFF'},
                {id:'1', color:'#CC0066'},
                {id:'1', color:'#000000'},
                {id:'1', color:'#FFFFFF'},
                {id:'1', color:'#AFFE00'},
                {id:'1', color:'#555555'},
                {id:'1', color:'#AAAAAA'},
                {id:'1', color:'#AABB55'},
                {id:'1', color:'#33FF99'},
                {id:'1', color:'#666933'},
                {id:'1', color:'#C69E00'},
                {id:'1', color:'#8EFFFF'},
                {id:'1', color:'#FF00AA'},
                {id:'1', color:'#AA00FF'},
                {id:'1', color:'#FFFF00'},
                {id:'1', color:'#FF7700'},
                {id:'1', color:'#CC99FF'},
                {id:'1', color:'#FF0000'},
                {id:'1', color:'#00FFFF'},
                {id:'1', color:'#CC0066'},
                {id:'1', color:'#000000'},
                {id:'1', color:'#FFFFFF'},
                {id:'1', color:'#FFFF00'},
                {id:'1', color:'#FF007F'},
                {id:'1', color:'#00FF00'},
                {id:'1', color:'#CC99FF'},
                {id:'1', color:'#FF0000'},
                {id:'1', color:'#00FFFF'},
                {id:'1', color:'#CC0066'},
                {id:'1', color:'#000000'},
                {id:'1', color:'#FFFFFF'}
            ]
        }
    }
}
</script>

<style scoped>
#colorbox{
    position: absolute;
    width: 180px;
    top: 30px;
    right: 9px;
    height: 200px;
    overflow-y: scroll;
}
.color{
    position: relative;
    float: right;
    border-style: solid;
    border-width: 0.1px;
    margin-left: 2px;
    margin-right: 2px;
    margin-top: 3px;
    z-index: 1;;
    width: 30px;
    height: 30px; 
}
</style>


