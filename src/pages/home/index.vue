<template>
  <view>
    <van-tabbar :active="active" @change="tabbarChange">
      <van-tabbar-item name="home" icon="home-o">首页</van-tabbar-item>
      <van-tabbar-item name="my" icon="user-circle-o">我的</van-tabbar-item>
    </van-tabbar>
  </view>
</template>

<script setup>
import { ref } from "vue";
const active = ref("home");
const tabbarChange = (event) => {
  active.value = event.detail;
};
</script>

<style lang="scss"></style>
