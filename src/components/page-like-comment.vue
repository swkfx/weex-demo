<template>
  <div>
    <div class="time-zan-views">
      <text class="time-text">今天 12:30</text>
      <image class="zan-comment-icon" />
    </div>

    <div class="zan-views">
      <div class="zan-view" v-for="(item) in data" :key="item">
        <text class="zan-texts">{{ item }}</text>
        <text> ,</text>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: ['asdasd','asdasd','qweqweqw','wodasvff','第五范式','按时打算大','奥飞机飞机']
    }
  },
}
</script>


<style scoped>
  .time-zan-views {
    flex-direction: row;
  }

  .zan-views {
    flex-direction: row;
    background-color: #fafafa;
    flex-wrap: wrap;
  }

  .zan-view {
    flex-direction: row;
  }

  .zan-texts {
    font-size: 14wx;
    color: lightgray;
  }

  .time-text {
    font-size: 12wx;
    color: gray;
    flex: 1;
  }

  .zan-comment-icon {
    background-color: aquamarine;
    width: 14wx;
    height: 14wx;
    margin-right: 16wx;
  }
</style>
