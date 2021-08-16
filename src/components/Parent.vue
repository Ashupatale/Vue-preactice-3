<template>
    <div>
            <h1>LifeCycle methods</h1> 

        <h3>Parent Comp</h3>
        <button @click="showChild= !showChlid">Toggle Child</button>
        <Child v-if="showChild"/>
    </div>
</template>

<script>
import Child from './Child.vue'

    export default {
        name:'Parent',
         components:{
            Child,
        },
        data(){
            return {
                showChild:true,
            }
        },
        
         beforeCreate(){
            console.log('Parent Before Create')
        },

         created(){
            console.log('Parent created')
        },
         beforeMount(){
            console.log('Parent Before Mount')
        },
         Mounted(){
            console.log('Parent  Mounted')
        },
         beforeUpdate(){
            console.log('Parent Before Update')
        },
         Upadted(){
            console.log('Parent  Updated')
        },
         beforeUnmount(){
            console.log('Parent Before Unmounting')
        },
         Unmounted(){
            console.log('Parent  Unmounted')
        },
        
    }
</script>

<style scoped>

</style>