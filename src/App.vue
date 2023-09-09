<template>
 <h1>{{ title }}</h1>
 <p>Welcome....</p>
<div v-if="showModal">
  <modal theme="sale" @close="toggleModal">
    
    </modal>
</div>
<button @click.alt="toggleModal">open Modal(alt)</button>
</template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',
  components:{ Modal },
data(){
  return{
    title:'My first Vue App :)',
    header:'Sign up here',
    text:'Grab your copy',
    showModal:false
  }
},
methods: {
  toggleModal(){
    this.showModal = !this.showModal
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
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
