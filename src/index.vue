<template>
  <div class="root-container">
    <div class="header-view">
      <div class="header-tab-item" @click="onClick(0)">
       <text class="header-tab-item-text-normal" :class="[ select === 0 ? 'header-tab-item-text-selected' : '']">时间</text>
      </div>
      <div class="header-tab-item" @click="onClick(1)">
       <text class="header-tab-item-text-normal" :class="[ select === 1 ? 'header-tab-item-text-selected' : '']">行为</text>
      </div>
      <div class="header-tab-item" @click="onClick(2)">
       <text class="header-tab-item-text-normal" :class="[ select === 2 ? 'header-tab-item-text-selected' : '']">人</text>
      </div>
    </div>
    <time-line-list class="list" v-if="select === 0"></time-line-list>
    <action-list class="list" v-if="select === 1"></action-list>
    <person-list class="list" v-if="select === 2"></person-list>
  </div>
</template>

<script>
import TimeLineList from "./components/time-line-list.vue";
import ActionList from "./components/action-list.vue";
import PersonList from "./components/person-list.vue";

export default {
  components: {
    TimeLineList,
    ActionList,
    PersonList,
  },
  data() {
    return {
      select: 1
    };
  },
  created() {},
  methods: {
    onClick(index) {
      this.select = index;
      console.log(index);
    }
  }
};
</script>

<style scoped>
.root-container {
  background-color: #efeff4;
}
.header-view {
  flex-direction: row;
  background-color: #fff;
  border-bottom-color: #e5e5e5;
  border-bottom-width: 1wx;
  border-bottom-style: solid;
}

.header-tab-item {
  flex: 1;
  align-items: center;
}

.header-tab-item-text-normal {
  padding-top: 10wx;
  padding-bottom: 10wx;
  font-size: 14wx;
  width: 120px;
  text-align: center;
}

.header-tab-item-text-selected {
  color: #7ea3ff;
  border-bottom-color: #7ea3ff;
  border-bottom-style: solid;
  border-bottom-width: 2wx;
}
</style>
