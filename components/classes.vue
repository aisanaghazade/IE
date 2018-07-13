<template>
    <div id = "class">
        <div id="subclass2">
            <div v-for="s in subclass" :key="s" class="subclass3" v-on:click="scview">
                <button class="button">{{s.name}}</button>
            <subclass1 v-if="b != true" class="subclass4"></subclass1>
            
            </div>
        </div>
    </div>
</template>
<script>
import subclass1 from '@/components/subclass1'

export default {
    components:{
         subclass1
    }, 
    props: [{'b':true}],
    data() {
        return{
        subclass:[
            {address:'#', name:'مردانه'},
            {address:'#', name:'زنانه'}
        ]
        }
    },
    methods: {
        scview:function(){
            this.b = !b;
        }
    }
  
}

</script>

<style scoped>
.subclass3{
    
    color: rgb(80, 80, 80);
    font-size: 100%;
}
.button{
    border-style: none;
    border-color: rgba(241,245,248);
    padding: 0px;
    background-color: rgba(241,245,248);
}



</style>



