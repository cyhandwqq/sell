<template>
  <div>
    <v-header :seller="seller"></v-header>
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
import './common/scss/common.css'
import Header from './components/header/header'
import Tab from './components/tab/tab'
// import Content from './components/content/content'
const ERR_OK = 0;
export default {
  name: 'app',
  data() {
    return {
      seller:''
    }
  },
  created() {
    var that = this;
    this.$http.get("/api/seller").then( (res) => {
      res = res.body;
      console.log(res);
      if(res.errno === ERR_OK) {
        that.seller = res.data;
        console.log(that.seller)
      }
    })
  },
  components:{
    'v-header' : Header,
    'v-tab' : Tab,
    // 'v-content' : Content
  }
}
</script>