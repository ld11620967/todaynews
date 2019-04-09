<template>
  <div>
    <ul class="list">
      <li v-for="item in list">
        <el-col :span="12">
          <div>{{item.title}}</div>
          {{item.published_at}}
        </el-col>
        <el-col :span="6">
          <img
            src="http://www.apkbus.com/data/attachment/forum/201805/21/121202u14siar8gzw5ekw4.jpeg"
            height="160px"
          >
        </el-col>
        <el-col :span="6">
          <div style="background:#f9fafc;height:3em;line-height:3em">热门文章</div>
        </el-col>
        <!-- <router-link :to="'/news/'+item._id">{{item.desc}}</router-link>
        <router-link :to="'/news/'+item._id">{{item.url}}</router-link>-->
      </li>
    </ul>
  </div>
</template>

<script>
//第三方插件的使用
import Axios from "axios";
export default {
  data() {
    return {
      list: []
    };
  },
  methods: {
    getData() {
      var api = "http://gank.io/api/xiandu/data/id/appinn/count/20/page/1";
      Axios.get(api)
        .then(response => {
          //console.log(response.data.result);
          this.list = response.data.results;
        })
        .catch(error => {
          console.log(error);
        });
    }
  },
  mounted() {
    this.getData();
  }
};
</script>

<style lang="scss" scoped>
.list {
  li {
    display: block;
    text-align: left;
    padding: 10px 0;
  }
}
</style>