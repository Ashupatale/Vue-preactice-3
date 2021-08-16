<template>
    <div>
        <h1 type="button" @mouseover="Increment">Increment {{count}} Times</h1> 
    </div>
</template>

<script>
import Countermixin from '../mixins/Counter'
    export default {
        name:'ClickCounter',
        mixins:[Countermixin],
       
        
    }
</script>

<style scoped>

</style>