<template>
  <footer>
    <div class="footer">
      <router-link to="/msite" :class="{cur: isCurrent('/msite')}">
        <i class="iconfont icon-waimaixinxi"></i>
        <span>用户</span>
      </router-link>
      <router-link to="/search" :class="{cur: isCurrent('/search')}">
        <i class="iconfont icon-tansuofaxian"></i>
        <span>搜索</span>
      </router-link>
      <router-link to="/order" :class="{cur: isCurrent('/order')}">
        <i class="iconfont icon-dingdanjilu"></i>
        <span>订单</span>
      </router-link>
      <router-link to="/profile" :class="{cur: isCurrent('/profile')}">
        <i class="iconfont icon-gaiicon-"></i>
        <span>个人</span>
      </router-link>
    </div>
  </footer>
</template>

<script>
export default {
  methods: {
    isCurrent (routPath) {
      return this.$route.path === routPath
    }
  }
}
</script>

<style>
.footer {
  border-top: 1px solid #e4e4e4;
  position: fixed;
  z-index: 100;
  left: 0;
  right: 0;
  bottom: 0;
  width: 100%;
  height: 50px;
  background-color: #ffffff;
  display: flex;
}
.footer a {
  width: 25%;
  display: flex;
  align-items: center;
  justify-content: center;
  flex-flow: column;
}
.footer a span {
  display: inline-block;
  margin-top: 4px;
  font-size: 13px;
}
.footer a i {
  font-size: 24px;
}
.footer .cur {
  color: #02a774;
}
</style>
