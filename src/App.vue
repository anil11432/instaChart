<template>
  <div id="app">
    <div class="col-md-12">
      <Insta/>
    </div>
    <div class="col-md-6">
      <InstaFollows/>
    </div>
    <div class="col-md-6">
      <InstaDiffrence/>
    </div>
  </div>
</template>

<script>
import Insta from './components/Insta';
import InstaFollows from './components/InstaFollows';
import InstaDiffrence from './components/InstaDiffrence';

export default {
  name: 'app',
  components: {
    Insta, InstaFollows, InstaDiffrence
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
