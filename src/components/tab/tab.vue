<template>
  <div class="tab">
    <div class="tab-items">
    	<router-link to="/goods">商品</router-link>
    </div>
    <div class="tab-items">
    	<router-link to="/ratings">评论</router-link>
    </div>
    <div class="tab-items">
    	<router-link to="/seller">商家</router-link>
    </div>
  </div>
</template>

<script>
export default {
  name: 'tab',
  data () {
    return {
      msg: '我是 tab'
    }
  }
}
</script>
<style lang="scss">
	.tab {
		display: -webkit-box;
		display: -ms-flexbox;
		display: flex;
		width: 100%;
		height: 40px;
		line-height: 40px;
		.tab-items {
			-webkit-box-flex: 1;
			-ms-flex: 1;
			flex: 1;
			text-align: center;
		}
	}
</style>
