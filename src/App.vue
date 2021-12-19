<template>
  <router-view />
  <div id="nav">
    <router-link to="/" class="tab-bar-item">
      <div class="icon"><i class="iconfont icon-home"></i></div>
      <div>首页</div>
    </router-link>
    <router-link to="/category" class="tab-bar-item">
      <div class="icon"><i class="iconfont icon-fenlei"></i></div>
      <div>分类</div>
    </router-link>
    <router-link to="/cart" class="tab-bar-item">
      <div class="icon"><i class="iconfont icon-gouwuche"></i></div>
      <div>购物车</div>
    </router-link>
    <router-link to="/profile" class="tab-bar-item">
      <div class="icon"><i class="iconfont icon-yonghu"></i></div>
      <div>个人中心</div>
    </router-link>
  </div>
</template>

<style lang="scss">
@import "assets/css/base.css";
@import "assets/css/iconfont.css";

#nav {
  background-color: #f6f6f6;
  display: flex;
  position: fixed;
  left: 0;
  right: 0;
  bottom: 0;
  box-shadow: 0 -3px 1px rgba(100, 100, 100, 0.1);
  a {
    color: var(--color-text);

    &.router-link-exact-active {
      color: #42b983;
    }
  }
  .tab-bar-item {
    flex: 1;
    text-align: center;
    height: 50px;
    font-size: var(--font-size);
    .icon {
      width: 24px;
      height: 24px;
      margin-top: 5px;
      vertical-align: middle;
      display: inline-block;
    }
  }
}
</style>
