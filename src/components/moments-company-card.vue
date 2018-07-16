<template>
  <div>
    <div class="box-flex-row box-margin">
        <image class="avatar" :src="data.headerUrl"/>
        <div class="left">
          <div class="box-flex-row box-company-title">
            <text class="company-name-text">{{ data.name }}</text>
            <image class="company-tag-img" src="/image/ic_v.png"/>
            <text class="company-tag-text">公司</text>
          </div>
          <div class="company-detail">
              <image class="company-detail-img" :src="data.urls[0]" resize="cover" />
              <text class="company-detail-title">{{ data.content }}</text>    
          </div>
          <div @click="onClick('http://www.baidu.com')" class="box-flex-row box-company-link">
            <text class="company-link-text">查看详情</text>
            <image class="company-link-img" src="/image/ic_link.png"/>
          </div>

          <page-like-comment></page-like-comment>
        </div>
    </div>
    <div class="line"></div>
  </div>
</template>

<script>
import PageLikeComment from './page-like-comment.vue'

const event = weex.requireModule("event");

export default {
  components: {
    PageLikeComment,
  },
  props: {
    data: {
      type: Object,
      default: {}
    }
  },
  methods: {
    onClick: function(url) {
      const pageUrl =
        "http://192.168.4.118:8081/dist/web-page.js?_wx_tpl=http://192.168.4.118:8081/dist/web-page.js";
      event.openURL(pageUrl);
      
    }
  }
};
</script>




<style scoped>
.box-flex-row {
  flex-direction: row;
}

.box-margin {
  padding: 12wx;
}

.avatar {
  margin-right: 12wx;
  width: 45wx;
  height: 45wx;
}

.box-company-title {
  align-items: center;
  padding-bottom: 16wx;
}

.company-name-text {
  padding-left: 8wx;
  padding-right: 12wx;
  color: #576b95;
  font-size: 14wx;
}

.company-tag-img {
  width: 16wx;
  height: 16wx;
  margin-right: 12wx;
}
.left {
  flex: 1;
}

.company-tag-text {
  padding-left: 8wx;
  padding-right: 8wx;
  padding-top: 0.5wx;
  padding-bottom: 0.5wx;
  font-size: 12wx;
  color: #9d9d9d;
  border-color: #9d9d9d;
  border-radius: 4wx;
  border-width: 1wx;
  border-style: solid;
}

.company-detail {
  background-color: #f3f3f3;
  padding: 8wx;
}

.company-detail-img {
  width: 544px;
  height: 436px;
}

.company-detail-title {
  font-size: 21wx;
  padding-top: 20wx;
  padding-bottom: 20wx;
  color: #2c3e50;
  font-weight: bold;
  lines: 1;
  text-overflow: ellipsis;
}

.box-company-link {
  padding-top: 12wx;
  align-items: center;
}

.company-link-text {
  font-size: 14wx;
  color: #566a94;
}

.company-link-img {
  width: 16wx;
  height: 16wx;
}

.line {
  height: 1wx;
  background-color: #efeff4;
}
</style>
