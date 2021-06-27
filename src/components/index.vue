<template>
  <div id="mainContainer" class="mainContainer">
    <div class="full">
      <div class="bg-img"></div>
      <background v-show="showBackground" class="particleBackground" dot-color="#FFF"></background>
      <header>
        <span class="title">CMK工作室</span>
      </header>
      <div class="content">
        <h1>Hello, World!</h1>
        <h1>CMK工作室</h1>
      </div>
    </div>
    <div class="settingsButton el-icon-setting" @click="visible = !visible"></div>
    <el-popover placement="left" trigger="manual" v-model="visible" popper-class="poper">
      <div class="settingsItem" @click="showBackground = !showBackground">显示特效</div>
    </el-popover>
  </div>
</template>

<script>
import particleBackground from './particleBackground'
export default {
  name: 'index',
  components: {
    background: particleBackground
  },
  data () {
    return {
      visible: false,
      showBackground: true
    }
  }
}
</script>

<style src="../style/index.less" lang="less"></style>
