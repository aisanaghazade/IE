<template>
    <div id="subclass1">
        <div v-for="s in subclass" :key="s" class="subclass">
            <button class="button">{{s.name}}<br></button>
        <subclass2 v-if="b != true"></subclass2>
        </div>
    </div>
</template>

<script>


import subclass2 from '@/components/subclass2'

export default {
    components:{
         subclass2
    }, 
    props: [{'b':true}],
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
    #subclass1{
        position: relative;
        right: 40px;
    }
    .subclass{
        font-size: 90%;
        color: rgb(126, 126, 126);
    }
    .subclass:hover{
        text-decoration: none;
        color: rgb(126, 126, 126);
    }
    .button{
        border-style: none;
        border-color: rgba(241,245,248);
        padding: 0px;
        background-color: rgba(241,245,248);
    }
</style>
