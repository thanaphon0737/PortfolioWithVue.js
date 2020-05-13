<template>
  <div id="app">
    <Header/>
    <h1>{{title}}</h1>
    <Content/>
    <Footer  title="Copyright 2020 by Thanaphon Thanusan Computer Engineering,CMU Tel:082-039-1362"/>
    <Clock>
      <span style="color:green;">current time</span>
    </Clock>
    
  </div>
</template>

<script>
import Header from "../src/components/layout/Header.vue"
import Footer from "../src/components/layout/Footer.vue"
import Content from "../src/components/layout/Content.vue"
import Clock from "../src/components/layout/Clock.vue"
export default {
  name: 'app',
  data() {
    return {
      title:'Portfolio',
      
    }
  },
  components:{
    Header,
    Footer,
    Content,
    Clock,
  }
}
</script>

<style scpoed>
  
  

  
</style>