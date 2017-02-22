<template>
  <div class="header">
    <div class="content-wrap">
    	<div class="avatar">
    		<img :src="seller.avatar" alt="" width="64" height="64" />
    	</div>
    	<div class="content vt">
    		<div class="title">
    			<span class="brand disib"></span>
    			<span class="name disib">{{seller.name}}</span>
    		</div>
    		<div class="description">
    			{{seller.description}}/{{seller.deliveryTime}}分钟送达
    		</div>
    		<div v-if="seller.supports" class="support">
    			<span class="icon"></span>
    			<span class="text">{{seller.supports[0].description}}</span>
    		</div>
    	</div>
    </div>	
    <div class="bulletion-wrap"></div>	
  </div>
</template>

<script>
export default {
  name: 'header',
  props:['seller'],
  data () {
    return {
      msg: '我是 header'
    }
  }
}
</script>
<style lang="scss">
@import './header.scss';
@import '../../common/scss/plugin.scss';
.header {
	color: #fff;
	background: #000;
	.content-wrap {
		padding: 24px 12px 18px 24px;
		font-size: 0;
		.avatar {
			display: inline-block;
			margin-right: 16px;
		}
		.content {
			display: inline-block;
			vertical-align: top;
			font-size: 1.2rem;
			.title {
				margin: 2px 6px 8px 0;
				.brand {
					display: inline-block;
					vertical-align: top;
					width: 3rem;
					height: 1.8rem;
					margin: 0 6px 0 0;
					@include retinize("brand","png");
					background-size: 30px 18px;
				}
			}
			.name {
				font-size: 1.6rem;
				font-weight: 700;
				line-height: 18px;
			}
			.description {
				margin-bottom: 10px;
				font-size: 1.2rem;
				line-height: 1.2rem;
			}
			.support {
				font-size: 1rem;
			}

		}

	}
}
</style>
