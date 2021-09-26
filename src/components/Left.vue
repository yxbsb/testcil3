<template>
  <div>
    <div class="title">热门推荐</div>
    <ul class="menu">
      <li @click="menu1">笔记本电脑1</li>
      <li @click="menu2">笔记本电脑2</li>
      <li @click="menu3">笔记本电脑3</li>
      <li @click="menu4">笔记本电脑4</li>
      <li>笔记本电脑5</li>
      <li>笔记本电脑6</li>
      <li>笔记本电脑7</li>
      <li>笔记本电脑8</li>
      <li>笔记本电脑9</li>
      <li>笔记本电脑10</li>
    </ul>
  </div>
</template>
<style scoped>
.title {
  width: 100px;
  color: red;
}
.menu li {
  margin-left: -50px;
  list-style: none;
  height: 50px;
  margin-bottom: 2px;
  background-color: white;
  line-height: 50px;
  cursor: pointer;
}
</style>
<script>
import Msg from "./msg.js";
export default {
  methods: {
    menu1: function () {
      Msg.$emit("val", "1");
    },
    menu2: function () {
      Msg.$emit("val", "2");
    },
    menu3: function () {
      Msg.$emit("val", "3");
    },
    menu4: function () {
      Msg.$emit("val", "4");
    },
  },
};
</script>