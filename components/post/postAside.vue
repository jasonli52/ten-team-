<template>
  <div class="postAside">
    <el-row>
      <div class="rec_nav" v-for="(item,index) in recNav" :key="index">
        <span>{{item.type}}</span>
        <i>></i>
      </div>

      <div class="navList"></div>
    </el-row>

    <div class="line"></div>

    <h3>推荐城市</h3>

    <a href="javascript:;">
      <img src="http://157.122.54.189:9093/images/pic_sea.jpeg" alt />
    </a>
  </div>
</template>

<script>
export default {
  data() {
    return {
      recNav: []
    };
  },
  mounted() {
    this.$axios({
      url: "posts/cities"
    }).then(res => {
      this.recNav = res.data.data;
    });
  }
};
</script>

<style lang="less" scoped>
.rec_nav {
  display: flex;
  justify-content: space-between;
  padding: 0 20px;
  width: 220px;
  height: 40px;
  line-height: 40px;
  border: 1px solid #ccc;
  border-bottom: none;
}
.rec_nav:hover{
  color: #ffa500;
  border-right: none;
}
.navList {
  z-index: 9999;
  position: absolute;
  top: 0;
  left: 262px;
  width: 300px;
  height: 200px;
  background: white;
  border: 1px solid #ccc;
  border-left:none;
}
.line {
  width: 260px;
  height: 0.5px;
  background: #ccc;
}
h3 {
  width: 260px;
  height: 40px;
  line-height: 40px;
  margin-top: 20px;
  font-weight: normal;
  border-bottom: 1px solid #ccc;
}
img {
  margin-top: 20px;
  width: 260px;
  height: 175px;
}
</style>
