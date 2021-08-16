<template>
    <div>
        <h3>Child Components</h3>
    </div>
</template>

<script>
    export default {
        name:'Child',
        beforeCreate(){
            console.log('Child Before Create')
        },

         created(){
            console.log('Child created')
        },
         beforeMount(){
            console.log('Child Before Mount')
        },
         Mounted(){
            console.log('Child  Mounted')
        },
         beforeUpdate(){
            console.log('Child Before Update')
        },
         Upadted(){
            console.log('Child  Updated')
        },
         beforeUnmount(){
            console.log('Child Before Unmounting')
        },
         Unmounted(){
            console.log('Child  Unmounted')
        },
        

    }
</script>

<style scoped>

</style>