<template>
  <div class="index">
    <div class="sp">
      <span
        v-for="(item,index) in item"
        :key="index"
        @click="hander(index)"
        :class="{act : cur === index}"
       class="divs">{{item}}</span>
    </div>
    <div v-show="cur === 0" >
      <ul>
        <li >撒酒疯</li>
      </ul>
    </div>
    <div v-show="cur === 1">
      <ul>
        <li>sadf</li>
      </ul>
    </div>
    <div v-show="cur === 2">
      <ul>
        <li>asflaslxz</li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      item: ["新闻", "体育", "娱乐"],
      cur: 0
    };
  },
  methods: {
    hander(index) {
      this.cur = index;
    }
  }
};
</script>

<style lang="less" scoped>
.act {
  color: red;
}
.sp{
  margin-bottom: 15px;
  span {
    cursor: pointer;
  }
}
.divs{
  margin-left:15px
}
</style>

