<template>
    <div id = "class">
        <div id="subclass2">
            <a v-for="s in subclass" :key="s" href="#" class="subclass3">{{s.name}}
            <subclass1 class="subclass4"></subclass1>
            
            </a>
        </div>
    </div>
</template>
<script>
import subclass1 from '@/components/subclass1'

export default {
    components:{
         subclass1
    }, 
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
.subclass3{
    
    color: rgb(80, 80, 80);
}



</style>



