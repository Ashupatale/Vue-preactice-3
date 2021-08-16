<template>
<div>

  <div id="app">
        <h2>Dynmaic Components </h2>

    <button @click="activeTab= 'CompA'">Comp A</button>
     <button @click="activeTab= 'CompB'">Comp B</button>
    <button @click="activeTab= 'CompC'">Comp C</button>

<keep-alive>
  <component :is="activeTab"/>
</keep-alive>
<hr/>
  <h2>HTTP Requests by Get and Post Methods</h2>
  
<PostList/>

<p>

  <CreatePost/>
</p>
<hr/>
<Parent/>
</div>
<TemplateRef/>

<ClickCounter/>

<HoverCounter/>

<Data/>
</div>
</template>



<script>
import CompA from './components/CompA.vue'
import CompB from './components/CompB.vue'
import CompC from './components/CompC.vue'
import PostList from './components/PostList.vue'
import CreatePost from './components/CreatePost.vue'
import Parent from './components/Parent.vue'
import TemplateRef from './components/TemplateRef.vue'
import ClickCounter from './components/ClickCounter.vue'
import HoverCounter from './components/HoverCounter.vue'
import Data from './components/Data.vue'

export default {
name: 'App',
  components: {
    CompA,
    CompB,
    CompC,
    PostList,
    CreatePost,
    Parent,
    TemplateRef,
    ClickCounter,
    HoverCounter,
    Data,

  },
  data(){
    return {
      activeTab:'CompA',
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
