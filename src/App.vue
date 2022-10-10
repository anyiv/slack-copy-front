<template>
  <div id="app">
      <top-bar/>
      <div class="title">Make teamwork more productive</div>
      <div class="d-flex">
        <router-view />
      </div>
      
  </div>
</template>

<script>
import TopBar from './components/Barra.vue'

export default {
  components: {
    TopBar
    
  },
  data(){
    return {
                isLoading: false,
                isFullPage: true
            }
  }
  
}
</script>

<style>
#app{
  background-color: #F9F0FA;
}
.d-flex{
display: flex;
}
.title{
  margin-top: 2.5em;
  text-align: center;
}
</style>