<template>
<div>
    <div>   
        <label for="name">Enter Name</label>
        <input type="text" ref="InputRef" />
        
    </div>
    <div>
        <PostList  ref="PostListRef"/>

    </div>
</div>
</template>

<script>
import PostList from './PostList.vue'

    export default {
        name:'TemplateRef',
        components:{
            PostList,

        },
        mounted(){
            console.log(this.$refs.PostListRef)
            this.$refs.InputRef.focus();
        }
      
    }
</script>

<style scoped>

</style>