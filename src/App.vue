<template>
  <div id="app">
    <Predictor/>
    <Converter/>
    <Translater/>
    <LoginandPass/>
  </div>
</template>

<script>

import Predictor from './components/Predictor';
import Converter from './components/Converter';
import Translater from './components/Translater';
import LoginandPass from './components/LoginandPass';

export default {
  name: 'App',
  components: {
    Predictor,
    Converter,
    Translater,
    LoginandPass
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #86b9eb;
  margin-top: 60px;
}
</style>
