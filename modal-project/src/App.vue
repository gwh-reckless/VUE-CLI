<template>
  <h1>{{  title  }}</h1>
  <h2>Just Test</h2>
  <img src="./assets/logo.png" alt="">
  <br>
  <!-- define a ref called boo here -->
  <input type="text" ref="boo">
  <button @click="handleClick">click me</button>
  <Modal v-if="showModal"/>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: 'App',
  data(){
    return {
      title: 'My First Vue App: )',
      showModal: false
    }
  },
  methods: {
    handleClick(){
      // use the ref called boo
      // this.$refs.boo.classList.add('active')
      // this.$refs.boo.focus();
      this.showModal = true;
    }
  },
  components: {
    Modal
  }
};
</script>

<style >
/* Notice: the app styles can not be scoped, because it's actually not in this component */
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

h1 {
  color: lightblue;
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
