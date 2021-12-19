<template>
  <div class="nav-bar">
    <div class="left" @click="goBack">
      <slot name="left">
        <img src="~assets/images/Left.png" alt="" />
      </slot>
    </div>
    <div class="center"><slot>图书商城</slot></div>
    <div class="right"><slot name="right"></slot></div>
  </div>
</template>

<script>
import { useRouter } from "vue-router";
export default {
  setup() {
    const router = useRouter();
    const goBack = () => {
      router.go(-1)
    }

    return { goBack }
  }
}
</script>

<style lang="scss" scoped>
.nav-bar {
  width: 100%;
  background-color: var(--color-tint);
  color: #fff;
  position: fixed;
  left: 0;
  top: 0;
  z-index: 9;
  height: 45px;
  line-height: 45px;
  text-align: center;
  box-shadow: 0 2px 0 rgba(100, 100, 100, 0.1);
  display: flex;
  .left,
  .right {
    width: 60px;
  }
  .left img {
    width: 45px;
    padding: 12px;
  }
  .center {
    flex: 1;
  }
}
</style>