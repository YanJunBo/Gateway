<template>
  <div>
    <el-header>
      <div class="df f-ac">
        <div class="logo fg-3">Logo</div>
        <el-menu
          mode="horizontal"
          class="fg-1"
          :default-active="activeIndex"
        >
          <el-menu-item index="1">网站首页</el-menu-item>
          <el-menu-item index="2">服务项目</el-menu-item>
          <el-menu-item index="3">作品展示</el-menu-item>
          <el-menu-item index="4">服务团队</el-menu-item>
          <el-menu-item index="5">联系我们</el-menu-item>
        </el-menu>
      </div>
    </el-header>
    <div>
      <el-carousel indicator-position="outside" height="490px">
        <el-carousel-item
          v-for="item in sliderImages"
          :key="item.url"
        >
          <div
            class="sliderImage"
            v-bind:style="{backgroundImage:'url(' + item.url + ')'}"
          ></div>
        </el-carousel-item>
      </el-carousel>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeIndex: "1",
      sliderImages:[{
          url:"http://www.qkhtml.com/Uploads/Picture/2015-11-05/563afb4385f14.jpg"
      },{
          url:"http://www.qkhtml.com/Uploads/Picture/2018-05-16/5afb8f3ae5218.jpg"
      },{
          url:"http://www.qkhtml.com/Uploads/Picture/2018-09-27/5bac9c70df4e3.jpg"
      }]
    };
  }
};
</script>

<style scoped>
.el-menu.el-menu--horizontal {
  border: none;
}
.el-carousel__item h3 {
  color: #475669;
  font-size: 18px;
  opacity: 0.75;
  line-height: 300px;
  margin: 0;
}
.el-carousel__item:nth-child(2n) {
  background-color: #99a9bf;
}

.el-carousel__item:nth-child(2n + 1) {
  background-color: #d3dce6;
}
.sliderImage {
  height: 100%;
  width: 100%;
  background-position: center center;
  background-size: cover;
  background-repeat: no-repeat;
}
</style>
