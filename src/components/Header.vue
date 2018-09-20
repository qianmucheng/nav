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
          <div class="bdsharebuttonbox">
            <!-- <a href="#" class="bds_more" data-cmd="more"></a> -->
            <a href="#" class="bds_weixin" data-cmd="weixin" title="分享到微信"></a>
            <a href="#" class="bds_sqq" data-cmd="sqq" title="分享到QQ好友"></a>
            <a href="#" class="bds_tsina" data-cmd="tsina" title="分享到新浪微博"></a>
            <a href="#" class="bds_tieba" data-cmd="tieba" title="分享到百度贴吧"></a>
          </div>
        </div>
      </el-col>
    </el-row>
  </div>
</template>

<script>
window._bd_share_config = {
  "common": {
    "bdSnsKey": { },
    "bdText": "",
    "bdMini": "2",
    "bdMiniList": false,
    "bdPic": "",
    "bdStyle": "1",
    "bdSize": "32"
  },
  "share": {}
};

export default {
  data() {
    return {
      website: "千木呈",
      navs: [{
        label: '轻松一刻',
        href: 'http://www.52rkl.cn',
      },{
        label: '关于',
        href: '#',
      }]
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
