<template>
  <div class="box-flex-row box-margin">
      <image class="avatar" src="http://www.qqzhi.com/uploadpic/2015-01-14/025418549.jpg"/>
      <div class="left">
        <div class="box-flex-row box-company-title">
          <text class="company-name-text">加推科技</text>
          <image class="company-tag-img" src="/image/ic_v.png"/>
          <text class="company-tag-text">公司</text>
        </div>
        <div class="company-detail">
            <image class="company-detail-img" src="https://p2.gexing.com/shaitu/20130203/1141/510ddc567c127.jpg"/>
            <text class="company-detail-title" lines="1">加推[名片电商]来了!开启'全...</text>    
        </div>
        <div @click="onClick('http://www.baidu.com')" class="box-flex-row box-company-link">
          <text class="company-link-text">查看详情</text>
          <image class="company-link-img" src="/image/ic_link.png"/>
        </div>
      </div>
  </div>
</template>

<script>
const event = weex.requireModule("event");

export default {
  methods: {
    onClick: function(url) {
      const pageUrl =
        "http://10.2.201.120:8081/dist/page/web-page.js?_wx_tpl=http://10.2.201.120:8081/dist/page/web-page.js%3fwebpage_url%3dhttp%3a%2f%2fwww.baidu.com";
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
  margin: 12wx;
}

.left {
  flex: 1;
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
  margin-right: 12wx;
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
</style>
