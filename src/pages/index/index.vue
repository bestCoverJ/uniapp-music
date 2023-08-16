<template>
  <view class="index-page">
    <image
      class="index-background-image"
      :src="backgroundImage"
      mode="aspectFill"
    />
    <view class="index-button-bar flex flex-direction align-center">
      <text class="text-white text-xxl text-bold">畅享音乐生活</text>
      <text class="text-gray text-center text-bold margin-bottom-lg"
        >在这里，随心畅听你最爱的内容，使用私人电台探索专属于你的音乐世界。</text
      >
      <button class="confirm-button cu-btn bg-mauve round lg" @click="toHome">
        快速开始
      </button>
    </view>
  </view>
</template>

<script setup>
import { useAppStore } from "@/store/index"
import backgroundImage from "@/static/images/cb62a8c75bf449a328c1eacaaf2554a4.jpg"
const app = useAppStore()

const toHome = () => {
  uni.login({
    success(res) {
      console.log(res)
      uni.reLaunch({
        url: "/pages/home/index",
      })
    },
  })
}
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
    background: linear-gradient(0deg, #000 0%, rgba(0, 0, 0, 0) 100%);
    z-index: 10;
    position: absolute;
    bottom: 0;
    left: 0;
    width: 100%;
    padding: 128rpx;
    gap: 48rpx;
    .confirm-button {
      width: 100%;
    }
  }
}
</style>
