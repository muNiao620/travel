<!-- 以vue结尾的文件就是单文件组件 -->
<template>
  <div id="app">
  	<keep-alive exclude="Detail">
    	<router-view/>
		</keep-alive>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style></style>
