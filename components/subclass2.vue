<template>
    <div id="subclass2">
        <a v-for="s in subclass" :key="s" href="#" class="subclass">{{s.name}}<br></a>
    </div>
</template>

<script>
export default {
    props: [],
    data() {
        return{
        subclass:[
            {address:'#', name:'مردانه'},
            {address:'#', name:'زنانه'}
        ]
        }
    }
}
</script>

<style scoped>
    #subclass2{
        width: 100;
        height: 100;
        position: relative;
        top: 0px;
        direction: rtl;
        right: 30px;
    }
    .subclass{
        color: rgb(167, 167, 167);
        direction: rtl;
        font-size: 90%;
        text-decoration: none;
    }
</style>

