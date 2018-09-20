<template>
  <div class="czp-main">
    <el-row :gutter="20">
      	<el-col class="nav-item" v-for="(item, index) in websites" :key="index" :span="6" :offset="index % 3 === 0 ? 2 : 1">
	        <div class="grid-content">
				<div>{{item.category}}</div>
	          	<el-row :gutter="2">
		          	<el-col v-for="(site, index2) in item.sites" :key="index2" :span="8" class="site">
		          		<a :href="site.link" target="_blank">{{site.name}}</a>
		          	</el-col>
	          	</el-row>
	        </div>
      	</el-col>
    </el-row>
  </div>
</template>

<script>
import websites from '../utils/website.js';

export default {
  data() {
    return {
    	websites: websites
    }
  }
}
</script>

<style scoped lang="less">
.czp-main {
	margin-top: 20px;
}

.nav-item {
    margin-bottom: 40px;
}

.grid-content {
	div {
		padding: 5px;
		font-size: 16px;
		text-align: left;
		color: #fff;
	}
}

.site {
	height: 50px;
	margin-bottom: 2px;
	a {
		display: block;
		height: 50px;
		line-height: 50px;
		text-align: center;
		text-decoration: none; 
		background-color: rgba(255, 255, 255, 0.8);
		cursor: point;
		color: #333;
		font-size: 14px;
		transition-property: background-color, color, font-size;
        transition-duration: 0.3s;
        transition-timing-function: ease;
		&:hover {
			background-color: #2c3e50;
			color: #fff;
			font-size: 18px;
		}
	}
}
</style>