<template>
  <view class="index">
    editor:
    <editor id="editor1" />
  </view>
</template>

<script lang="ts">
import Taro from '@tarojs/taro'
import './index.css'

export default {
  data() {
    return {
    }
  },
  mounted() {
    const page = Taro.getCurrentInstance().page
    // @ts-ignore
    page.createSelectorQuery().select('#editor1').context(res => {
      console.log(res)
      // null
    }).exec()

    Taro.createSelectorQuery().select('#editor1').context(res => {
      console.log(res)
      // null
    }).exec()
  }
}
</script>
