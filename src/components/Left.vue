<template>
  <el-row>
    <el-col :span="16">
      <div class="block">
        <!-- <span class="demonstration">Click 指示器触发</span> -->
        <el-carousel height="340px">
          <el-carousel-item v-for="item in 4" :key="item">
            <div>
              <a href="#" onclick="window.open('http://www.apkbus.com/thread-605543-1-1.html')">
                <img
                  src="http://www.apkbus.com/data/attachment/forum/201902/15/100118xoikij8db506u88m.jpg"
                  height="340px"
                  width="600px"
                >
                <div
                  style="position:absolute; z-index:2; left:30px; top:280px; color:white; font-weight:bold;font-size:18px"
                >添加文字...添加文字...添加文字...</div>
              </a>
            </div>
          </el-carousel-item>
        </el-carousel>
      </div>
    </el-col>
    <el-col :span="8">
      <div>
        <a href="#" onclick="window.open('http://www.apkbus.com/thread-605543-1-1.html')">
          <img
            src="http://www.apkbus.com/data/attachment/forum/201902/15/100118xoikij8db506u88m.jpg"
            height="170px"
          >
        </a>
      </div>
      <div>
        <a href="#" onclick="window.open('http://www.apkbus.com/thread-606490-1-1.html')">
          <img
            src="http://www.apkbus.com/data/attachment/forum/201903/18/121251ta441v91z44tlrnl.jpg"
            height="170px"
          >
        </a>
      </div>
    </el-col>
    <div>
      <ul class="list">
        <li v-for="item in list" :key="item">
          <el-col :span="16">
            <div>{{item.desc}}</div>
            {{item.publishedAt}}
          </el-col>
          <el-col :span="8">
            <img
              src="http://www.apkbus.com/data/attachment/forum/201805/21/121202u14siar8gzw5ekw4.jpeg"
              height="160px"
            >
          </el-col>
        </li>
      </ul>
    </div>
  </el-row>
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
      var api = "http://gank.io/api/today";
      Axios.get(api)
        .then(response => {
          //console.log(response.data.result);
          this.list = response.data.results.前端;
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

.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}
</style>