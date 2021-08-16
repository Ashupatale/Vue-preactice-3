<template>
    <div>
        
        <form @submit.prevent="createPost"> 
            <div>
            <label for="userId">User ID</label>
            <input type="text" id="userId"  v-model="formData.userId"/>
            </div>

             <div>
            <label for="title">title</label>
            <input type="text" id="title" v-model="formData.title"/>
            </div>

             <div>
            <label for="Body">Body</label>
            <input type="text" id="Body" v-model="formData.Body"/>
            </div>

            <button type="submit">Create Post</button>

        </form>

    </div>
</template>

<script>
import axios from 'axios'
    export default {
        name:'CreateList',
        data(){
            return{
                formData:{
                userId:'',
                title:'',
                Body:'',
                },
               
            }
        },
        methods:{
            createPost(){
                axios.post("https://jsonplaceholder.typicode.com/posts" , this.formData)
                .then(response=> console.log(response))
                .catch(error=> console.log(error)
                )
            }
        }
        
    }
</script>

<style scoped>

</style>