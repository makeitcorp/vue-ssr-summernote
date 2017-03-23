<template>
  <div class="main-content" id="app">
    <h1>서버사이드 렌더 테스트</h1>
    <router-view></router-view>
    <div id="summernote">Hello Summernote</div>
  </div>
</template>
<script>

export default {
  name: 'app',
  mounted () {
    if (typeof (window) !== 'undefined') {
      require('assets/js/bootstrap.js')
      require('assets/summernote.js')
    }

    $('#summernote').summernote()
  }
}
</script>

<style lang="scss" scoped>
@import 'assets/css/bootstrap.min.css';
@import 'assets/summernote.css';
  h1 {
    font-size:25px;
  }
</style>
