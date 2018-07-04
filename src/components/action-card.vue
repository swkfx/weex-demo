<template>
  <div class="card-box">
    <div class="card" v-for="item in items" :key="item.src">
      <image class="icon" :src="item.src"/>
      <div class="count-view">
        <text class="name-text">{{item.name || ""}}</text>
        <div class="count-box">
          <text class="count-text">{{item.count || 0}}</text>
          <text class="count-unit">次</text>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    items: {
      type: Array,
      default: []
    }
  }
};
</script>


<style scoped>
.card-box {
  flex-wrap :wrap;
  flex-direction: row;
  padding-top: 30px;
  padding-left: 30px;
  background-color: #fafafa;
  margin-bottom: 5wx;
}

.card {  
  width: 330px;
  padding: 10wx;
  flex-direction: row;
  background-color: #7096fe;
  border-radius: 5wx;
  margin-bottom: 30px;
  margin-right: 30px;
}

.icon {
  width: 50wx;
  height: 50wx;
}

.name-text {
  color: #ffffff;
  font-size: 14wx;
}

.count-view {
  margin-left: 4wx;
}

.count-box {
  flex-direction: row;
  align-items: flex-end;
}

.count-text {
  color: #ffffff;
  font-size: 14wx;
  line-height: 13wx;
  margin-top: 9wx;
}

.count-unit {
  color: #ffffff;
  font-size: 10wx;
}
</style>
