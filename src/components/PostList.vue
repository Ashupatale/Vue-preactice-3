<template>
<div>
    <div>
        <!-- <button type="button" class="btn" @click="getPost">Post Lists</button> -->
    </div>
    <div v-for="post in posts" :key="post.id" class="listDiv">
       
        <h3>{{post.id}} {{post.name}} - {{post.email}}</h3>
        <hr/>

    </div>
             <h1 v-if="errorMsg" class="errMsg">{{errorMsg}}</h1>

</div>
</template>

<script>
import axios from 'axios'
    export default {
        name:'PostLits',
        created(){
            this.getPost()
        },
        data(){
            return {
                posts:[],
                errorMsg:'',
            }
        },
        methods: {
            getPost(){
                axios.get("https://jsonplaceholder.typicode.com/users")
                .then((response)=>{
                    this.posts=response.data
                })
                .catch((error)=>{
                    console.log(error)
                    this.errorMsg='Oops...Something Went Wrong...!'
                })
            }
        }
    }
</script>

<style scoped>
.btn{
  
    margin-top: 2%;
    padding: 10px 30px;
    border-radius: 10px;
    border: none;
    outline: none;
    background-color:green;
    color:white;
    cursor: pointer;
}

.listDiv{
    text-align: center;
    justify-content: center;
}
.errMsg{
    justify-content: center;
    text-align: center;
    color: red;
}

</style>