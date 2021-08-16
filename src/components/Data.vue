<template>
    <div>
        <h2>Options - {{name}}</h2>
         <h2>Compostion Api- {{c_name}}  </h2>

    </div>
</template>

<script>
import {ref} from 'vue'

    export default {
        name:'Data',
        data(){
            return{
                name:'Aakash'
            }
        },

        setup(){
            const c_name=ref('Aakash')

            return{
                c_name,
        }
        }
        
    }
</script>

<style scoped>

</style>