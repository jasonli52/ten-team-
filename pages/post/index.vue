<template>
  <div class="postIndex">
    <el-row style="width:1000px;margin:0 auto">
      <el-col :span="8">
        <PostAside />
      </el-col>
      <el-col :span="16">
        <el-row>
          <PostHeader />
        </el-row>
        <el-row>
          <PostList />
        </el-row>
      </el-col>
    </el-row>
  </div>
</template>

<script>
import PostAside from "@/components/post/postAside.vue";
import PostHeader from "@/components/post/postHeader.vue";
import PostList from "@/components/post/postList.vue";
export default {
  components: {
    PostAside,
    PostHeader,
    PostList
  }
};
</script>

<style lang="less" scoped>
.postIndex {
  margin-top: 20px;
}
</style>



