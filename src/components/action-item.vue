<template>
<div>
  <div class="content-view">
    <image class="icon" :src="item.src" />
    <text class="name-text">{{ item.name }}</text>
    <div class="count-box">
      <text class="count-text">{{item.count || 0}}</text>
      <text class="count-unit">次</text>
    </div>
  </div>
  <div class="line"></div>
</div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object, 
      default: {}
    }
  }
};
</script>

<style scoped>
  .content-view {
    flex-direction: row;
    background-color: #fafafa;
    padding: 16wx;
    align-items: center;
  }

  .icon {
    width: 20wx;
    height: 20wx;
  }

  .name-text {
    font-size: 14wx;
    margin-left: 16wx;
    flex: 1;
  }

  .count-box {
    flex-direction: row;
    align-items: center;
  }

  .count-text {
    color: #7ea3ff;
    font-size: 18wx;
  }

  .count-unit {
    color: #7ea3ff;
    font-size: 10wx;
  }
  
  .line {
    background-color: #EEEEF4;
    height: 1wx;  
  }
  
</style>

