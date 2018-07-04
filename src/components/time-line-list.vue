<template>
   <list>
      <cell v-for="(item,index) in items" :key="index">
        <time-line-item :item="item"/>
      </cell>
      <cell>
        <text class="no-more-text">没有更多数据</text>
      </cell>
    </list>
</template>

<script>
import TimeLineItem from './time-line-item.vue'
export default {
  components: {
    TimeLineItem
  },
  data (){
    return{
      items: [{
        time: '昨天12:12',
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望'
      },
      {
        
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望,拉力查看你的名片11次,成交在望,拉力查看你的名片11次,成交在望'
      },
      {
        
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望'
      },
      {
        time: '昨天13:12',
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望'
      },
      {
        time: '昨天12:12',
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望'
      },
      {
        
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望'
      },
      {
        time: '昨天13:12',
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望'
      },
      {
        time: '昨天12:12',
        avaterUrl: 'http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg',
        content:'拉力查看你的名片11次,成交在望'
      }]
    }
  }
}
</script>


<style scoped>
.container{
  background-color: #efeff4;
}

.no-more-text {
  padding: 16wx;
  text-align: center;
  font-size: 16wx;
  color: grey;
}
</style>
