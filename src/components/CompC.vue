<template>
    <div>
        <h1>Comp C</h1>
              <img src="https://picsum.photos/200/303" />
              <br/>
              <input type="text" v-model="name" />

    </div>
</template>

<script>
    export default {
        name:'CompC',
        data(){
            return{
                name:''
            }
        }
    }
</script>

<style scoped>

</style>