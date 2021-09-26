<template>
  <div class="main">
    <div class="left">
      <Left></Left>
    </div>
    <div class="right">
      <div class="top">
        <img src="../../public/img/img.png" />
      </div>
      <div class="button">
        <Right></Right>
      </div>
    </div>
  </div>
</template>
<style scoped>
* {
  padding: 0;
  margin: 0;
}
.left {
  width: 130px;
  float: left;
  margin-right: 10px;
}
.right {
  width: 1000px;
  float: left;
  margin-left: 10px;
}
.main {
  width: 1200px;
  margin: 20px auto;
}
.top img {
  width: 1000px;
  height: 200px;
}
.left,
.right {
  background: #f5f5f5;
  height: 500px;
}
</style>
<script>
import Left from "../components/Left.vue";
import Right from "../components/Right.vue";
export default {
  components: {
    Left,
    Right,
  },
};
</script>