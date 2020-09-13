<template>
  <div id="app">
   <Login v-on:login-in="proc"/>
   <Reset/>
  </div>
</template>

<script>
import Login from './components/Login';
//import Reset from './components/Reset';
import axios from 'axios';

export default {
  name: 'App',
  components: {
   Login
 // Reset
  },
  methods:{
    proc(lgin) {
      const {eml , pw}=lgin;

      axios.post('',{
        eml,
        pw
      })
      .then()
      .catch(err => console.log(err));
    }
  }
}
</script>

<style >
  body{
    margin: 0px;
    padding: 0;
    background: #9C39E4;
    background-size: cover;
    background-position: center;
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
}
</style>