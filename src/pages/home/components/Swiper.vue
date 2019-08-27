<template>
	<div class="wrapper">
		<swiper :options="swiperOption">
	    <!-- slides -->
	    <swiper-slide v-for="item of swiperList" :key="item.id">
	    	<img class="swip-img" :src="item.imgUrl">
	    </swiper-slide>
	    <div class="swiper-pagination"  slot="pagination"></div>
	  </swiper>
  </div>
</template>

<script>
export default {
	name: 'HomeSwiper',
	data () {
		return {
			swiperOption: {
				pagination: '.swiper-pagination',
				loop: true
			},
			swiperList: [{
				id: '0001',
				imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20197/a4c27b0a5fc1d9e9e620225869089b12.jpg_750x200_e4720428.jpg'
			}, {
				id: '0002',
				imgUrl: 'http://mp-piao-admincp.qunarzz.com/mp_piao_admin_mp_piao_admin/admin/20198/eb3fdb7ff86de0160cafe76b6a6a8ee3.jpg_750x200_e6930e5c.jpg'
			}]
		}
	}
}
</script>

<style lang="stylus" scoped>
	.wrapper >>> .swiper-pagination-bullet-active
		background: #fff
	.wrapper
		overflow: hidden
		width: 100%
		height: 0
		padding-bottom: 31.25%
		.swip-img
			width: 100%
</style>