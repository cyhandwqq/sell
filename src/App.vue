<template>
  <div>
    <v-header></v-header>
    <v-tab></v-tab>
    <!-- <v-content></v-content> -->
    <div class="content-wrap">
      <keep-alive>
        <router-view></router-view>
      </keep-alive>
    </div>
  </div>
</template>

<script>
import './common/scss/base.css'
import Header from './components/header/header'
import Tab from './components/tab/tab'
// import Content from './components/content/content'
export default {
  name: 'app',
  components:{
    'v-header' : Header,
    'v-tab' : Tab,
    // 'v-content' : Content
  }
}
</script>

<style lang="scss">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

</style>
