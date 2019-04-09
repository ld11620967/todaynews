<template>
  <el-row>
    <el-col :span="12">
      <div class="block">
        <!-- <span class="demonstration">Click 指示器触发</span> -->
        <el-carousel trigger="click" height="340px">
          <el-carousel-item v-for="item in 4" :key="item">
            <h3>{{ item }}</h3>
          </el-carousel-item>
        </el-carousel>
      </div>
    </el-col>
    <el-col :span="6">
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
    <el-col :span="6">
      <div style="background:#f9fafc;height:3em;line-height:3em">热门文章</div>
    </el-col>
  </el-row>
</template>

<style>
.el-carousel__item h3 {
  color: #475669;
  font-size: 14px;
  opacity: 0.75;
  line-height: 150px;
  margin: 0;
}

.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
</style>