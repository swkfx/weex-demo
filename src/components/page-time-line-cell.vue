<template>
  <div>
    <div class="content-view">
      <image class="header-img" :src="data.headerUrl" />
      <div class="text-view">
        <text class="name-text">{{ data.name }}</text>
        <text v-if="data.content" class="content-text">{{ data.content }}</text>
        <div v-if="data.urls.length === 1" class="img-views">
          <image @load="onImageLoad" :style="[ {width:375 + 'px'},{height:imageHeight + 'px'}]" :src="data.urls[0]" />
        </div>

        <div v-else-if="data.urls.length === 4" class="img-views img-views-other">
          <image v-for="(item) in data.urls" class="img" resize="cover" :src="item" :key="item" />
        </div>

        <div v-else-if="data.urls"  class="img-views">
          <image v-for="(item) in data.urls" class="img" resize="cover" :src="item" :key="item" />
        </div>

        <page-like-comment></page-like-comment>
      </div>
    </div>
    
    <div class="line"></div>
  </div>
</template>

<script>
import PageLikeComment from './page-like-comment.vue'

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
  data() {
    return{
      imageHeight: 375,
    }
  },
  methods: {
    onImageLoad (event) {
      if (event.success) {
        this.imageHeight = 375/event.size.naturalWidth * event.size.naturalHeight;
      }
    }
  }
}
</script>


<style scoped>
  .content-view {
    padding: 16wx;
    flex-direction: row;
  }

  .header-img {
    width: 42wx;
    height: 42wx;
    background-color: aquamarine;
  }

  .name-text {
    font-size: 16wx;
  }

  .content-text {
    font-size: 16wx;
    margin-top: 8wx;
  }

  .text-view {
    margin-left: 16wx;
    flex: 1;
  }

  .img {
    width: 169px;
    height: 169px;
    margin-right: 16px;
    margin-bottom: 16px;
  }

  .img-views {
    flex-wrap: wrap;
    flex-direction: row;
    margin-top: 8wx;
  }

  .img-views-other {
    width: 370px;
  }

  .line {
    height: 1wx;
    background-color: #efeff4;
  }
</style>
