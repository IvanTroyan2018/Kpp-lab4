<template>
    <div id="app">
      <app-nav></app-nav>
      <transition name="fade" mode="out-in">
        <router-view/>
      </transition>
    </div>
</template>

<script>
import AppNav from './components/AppNav';


export default {
  name: 'app',
  components: {AppNav}
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

.fade-enter-active, .fade-leave-active {
  transition: opacity .5s;
}
.fade-enter, .fade-leave-to /* .fade-leave-active до версии 2.1.8 */ {
  opacity: 0;
}
</style>
