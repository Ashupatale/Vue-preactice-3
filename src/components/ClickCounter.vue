<template>
    <div>
        <button type="button" @click="Increment">Increment {{count}} Times</button> 
    </div>
</template>

<script>
import Countermixin from '../mixins/Counter'

    export default {
        name:'ClickCounter',
        mixins:[Countermixin],
        data(){
            return {
                count:100
            }
        }
       
        
    }
</script>

<style scoped>

</style>