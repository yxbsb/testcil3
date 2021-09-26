<template>
  <div class="show">
    <ul class="goodList">
      <li v-for="good in list">
        <img v-bind:src="good.img" />
        <p>{{ good.goodName }}</p>
      </li>
    </ul>
  </div>
</template>
<style scoped>
.goodList li {
  width: 190px;
  height: 190px;
  list-style: none;
  float: left;
  font-size: 9px;
  color: red;
  margin-bottom: 30px;
}
.goodList img {
  width: 180px;
  height: 180px;
}
</style>
<script>
export default {
  name: "show",
  data() {
    var obj = this;
    var url = "";
    if (obj.goodId == 1) {
      url = "../json/bjb.json";
    } else if (obj.goodId == 2) {
      url = "../json/sj.json";
    }
    this.$http.get(url).then(function (res) {
      obj.list = res.data;
    });
    return {
      list: [],
    };
  },
  props: {
    goodId: Number,
  },
  watch: {
    goodId() {
      var obj = this;
      var url = "";
      if (obj.goodId == 1) {
        url = "../json/bjb.json";
      } else if (obj.goodId == 2) {
        url = "../json/sj.json";
      }
      this.$http.get("../json/bjb.json").then(function (res) {
        obj.list = res.data;
      });
      return {
        list: [],
      };
    },
  },
};
</script>