<template>
    <div id="subclass1">
        <a v-for="s in subclass" :key="s" href="#" class="subclass">{{s.name}}<br>
        <subclass2></subclass2>
        </a>
    </div>
</template>

<script>


import subclass2 from '@/components/subclass2'

export default {
    components:{
         subclass2
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
    #subclass1{
        position: relative;
        right: 40px;
    }
</style>
