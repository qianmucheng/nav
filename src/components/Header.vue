<template>
  <div class="czp-header">
    <el-row :gutter="20">
      <el-col :span="4" :offset="2">
        <div class="grid-content desc" @click="refresh">
          <img src="../assets/images/logo.png">
          <h4>{{website}}</h4>
        </div>
      </el-col>
      <el-col :span="6">
        <div class="grid-content weather">
          <iframe name="weather_inc" src="http://i.tianqi.com/index.php?c=code&id=2&num=2" 
                  width="340" height="80" frameborder="0" marginwidth="0" 
                  marginheight="0" scrolling="no">
          </iframe>
        </div>
      </el-col>
      <el-col :span="6" :offset="4">
        <div class="grid-content nav">
          <share :config="share_config"></share>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
export default {
  data() {
    return {
      website: "千木呈",
      share_config: {
        url                 : 'https://qianmucheng.github.io/nav', // 网址，默认使用 window.location.href
        source              : '千木呈-导航', // 来源（QQ空间会用到）, 默认读取head标签：<meta name="site" content="http://overtrue" />
        title               : '千木呈-导航', // 标题，默认读取 document.title 或者 <meta name="title" content="share.js" />
        description         : '千木呈-导航', // 描述, 默认读取head标签：<meta name="description" content="PHP弱类型的实现原理分析" />
        sites               : ['wechat', 'qq', 'weibo', 'douban'], // 启用的站点
        wechatQrcodeTitle   : '微信扫一扫：分享', // 微信二维码提示文字
        wechatQrcodeHelper  : '<p>微信里点“发现”，扫一下</p><p>二维码便可将本文分享至朋友圈。</p>'
      }
    }
  },
  methods: {
    refresh() {
      window.location.reload();
    }
  }
}
</script>

<style scoped lang="less">
.czp-header {
  height: 100%;
  width: 80%;
  margin: 0 auto;
}
.grid-content {
  height: 80px;
}
.desc {
  display: table-cell;
  vertical-align: middle;
  text-align: center;
  cursor: pointer;
  img {
    height: 60px;
    width: 60px;
  }
  h4 {
    float: right;
    margin-left: 10px;
  }
}
.weather {
  i {
    float: right;
  }
}
.nav {
  box-sizing: border-box;
  margin: 0;
  padding: 18px 0;
  div {
    text-align: right;
    float: right;
    a {
      margin-left: 10px;
    }
  }
}
</style>
