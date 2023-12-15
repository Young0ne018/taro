<template>
  <view class="index">
    <Counter/>
  </view>
</template>

<script setup>
import './index.scss'
import Counter from '../../components/Counter.vue'
import Taro from "@tarojs/taro";
Taro.startLocationUpdateBackground({
  complete:(res)=>{
    console.log(res);
  }
})
Taro.onLocationChange((res)=>{
  console.log(res);
})
</script>
