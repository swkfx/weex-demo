<template>
  <div class="container">
    <div class="item-box">
      <image class="avatar" :src="item.avaterUrl"/>
      <text class="content">{{ item.content }}</text>
      <image class="arrow" src="/image/more.png"/>
    </div>
  </div>
</template>

<script>
export default {
  props:{
    item:{
      type: Object,
      default: {}
    }
  }

}
</script>

<style scoped>
  .container{
    padding-top: 16wx; 
    padding-left: 16wx; 
    padding-right: 16wx; 
  }

  .item-box{
    align-items:center;
    padding-top: 16wx;
    padding-bottom: 16wx;
    padding-left: 16wx;
    padding-right: 4wx;
    flex-direction: row;
    background-color: white;
    border-radius: 5wx;
    border-color: #f2f2f2;
    border-style: solid;
    border-width: 1wx;
  }
  .avatar{
    background-color: aqua;
    width: 38wx;
    height: 38wx;
    border-radius: 19wx; 
  }

  .content{
    margin-left: 10wx;
    font-size: 14wx;
    flex: 1;
  }

  .arrow {
    width: 18wx;
    height: 18wx;
  }
</style>
