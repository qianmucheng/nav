<template>
  <el-container>
    <el-header :style="{ left: scrollLeft + 'px'}">
      <Header></Header>
    </el-header>
    <el-main>
      <Main></Main>
    </el-main>
    <el-footer>
      <Footer></Footer>
    </el-footer>
  </el-container>
</template>

<script>
  import Header from '@/components/Header'
  import Main   from '@/components/Main'
  import Footer from '@/components/Footer'

  export default {
    components: {
      Header,
      Main,
      Footer
    },
    data() {
      return {
        scrollLeft: 0
      }
    },
    methods: {
      setScroll() {
        this.scrollLeft = -document.documentElement.scrollLeft;
      }
    },
    mounted() {
      window.addEventListener('scroll', this.setScroll)
    },
  }
</script>

<style lang="less">
body {
  margin: 0;
  padding: 0;
  background-color: #f5f5f5;
  min-width: 1200px;
  overflow: auto;
  background: red url('./assets/images/bg.jpg') no-repeat fixed;
}

.el-header {
  position: fixed;
  totp: 0;
  right: 0;
  left: 0;
  min-width: 1200px;
  box-shadow: 0 1px 5px #fff;
  z-index: 99;
  background-color: #fff;
  height: 80px !important;
  text-align: center;
  width: 100%;
}

.el-main {
  margin-top: 80px;
  text-align: center;
}

.el-footer {
  
}
</style>
