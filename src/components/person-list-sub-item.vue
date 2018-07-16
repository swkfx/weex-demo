<template>
  <div class="count-box">
    <div v-for="(subItem , index) in counts" :key="index" class="sub-item-box">
        <text>{{ subItem.name }}</text>
        <div class="progress"></div>
        <text>{{ subItem.count }}</text>
    </div>
  </div>  
</template>

<script>
export default {
  props: {
    counts: {
      type: Array,
      default: []
    }
  }
};
</script>


<style scoped>
.count-box {
  padding: 16wx;
}

.sub-item-box {
  flex-direction: row;
}

.progress {
  width: 20wx;
  height: 5wx;
  background-color: aqua;
  border-radius: 5wx;
}
</style>

