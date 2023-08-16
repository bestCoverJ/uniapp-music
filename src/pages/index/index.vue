<template>
  <view class="index-page">
    <image
      class="index-background-image"
      :src="backgroundImage"
      mode="aspectFill"
    />
    <div class="index-button-bar">
      <text>畅享音乐生活</text>
      <button @click="">快捷登录</button>
    </div>
  </view>
</template>

<script setup>
import { useAppStore } from "@/store/index"
import backgroundImage from "@/static/images/cb62a8c75bf449a328c1eacaaf2554a4.jpg"
const app = useAppStore()
</script>

<style lang="scss">
.index-page {
  height: 100vh;
  position: relative;
  .index-background-image {
    height: 100%;
    width: 100%;
    z-index: 1;
  }
  .index-button-bar {
    background: linear-gradient(0deg, #000 0%, rgba(0, 0, 0, 0.00) 100%);
    z-index: 10;
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 128rpx;
  }
}
</style>
