<template>
	<div class="czp-footer">
	    <div class="copyright">
	        <p>Copyright © 2018 <a href="#">千木呈</a> All Rights Reserved </p>
	    </div>
	</div>
</template>

<script>
export default {
  data() {
    return {

    }
  }
}
</script>

<style scoped lang="less">
.czp-footer {
	color: #fff;
	.copyright {
		margin: 0 auto 40px;
    	text-align: center;
    	white-space: nowrap;
    	cursor: default;
    	a {
    		text-decoration: none;
    		&:hover {
    			color: red;
    		};
    	}
	}
}
</style>