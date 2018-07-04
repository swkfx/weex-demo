<template>
   <list>
     <cell>
      <item-header/>
     </cell>
     <cell>
       <action-card :items="cardItems"/>
     </cell>

     <cell v-for="(item,index) in listItems" :key="index">
       <action-item :item="item"></action-item>
     </cell>
   </list>
</template>

<script>
import ActionCard from './action-card.vue';
import ActionItem from './action-item.vue';
import ItemHeader from './item-header.vue';

export default {
  components: {
    ActionCard,
    ActionItem,
    ItemHeader,
  },
  data (){
    return {
      cardItems:[{
        src: '/image/product.png',
        name: '查看商品',
        count: 21,
      },
      {
        src: '/image/guanwang.png',
        name: '查看官网',
        count: 6,
      },
      {
        src: '/image/wechat.png',
        name: '复制微信',
        count: 0,
      },
      {
        src: '/image/mingp.png',
        name: '发送名片',
        count: 2,
      }],
      listItems:[{
        src: '/image/ic_card.png',
        name: '查看名片',
        count: 22,
      },
      {
        src: '/image/ic_dontai.png',
        name: '看动态',
        count: 8,
      },
      {
        src: '/image/ic_product.png',
        name: '咨询产品',
        count: 2,
      },
      {
        src: '/image/ic_phone.png',
        name: '保存电话',
        count: 1,
      },
      {
        src: '/image/ic_kp.png',
        name: '觉得靠谱',
        count: 2,
      },
      {
        src: '/image/ic_call.png',
        name: '拨打电话',
        count: 1,
      },
      {
        src: '/image/ic_voice.png',
        name: '播放语音',
        count: 0,
      },
      {
        src: '/image/ic_mail.png',
        name: '复制邮箱',
        count: 0,
      }]
    }
  }
}
</script>


