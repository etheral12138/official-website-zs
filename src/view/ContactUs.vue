<template>
  <div id="ContactUs">
    <div class="banner container-fuild text-center">{{ $t('contact') }}</div>
    <div class="container">
      <div class="container-fuild ContactUs-container">
        <div class="row">
          <div class="col-xs-12 col-sm-12">
            <form class="form-horizontal" role="form">
              <div class="form-group">
                <label class="col-sm-2 control-label" for="name">{{ $t('name') }}</label>
                <div class="col-sm-10 col-xs-12">
                  <input id="name" class="form-control" placeholder="请输入名字" type="text">
                </div>
              </div>
              <div class="form-group">
                <label class="col-sm-2 control-label" for="email">{{ $t('email') }}</label>
                <div class="col-sm-10">
                  <input id="email" class="form-control" placeholder="请输入邮箱" type="text">
                </div>
              </div>
              <div class="form-group">
                <label class="col-sm-2 control-label" for="tel">{{ $t('tel') }}</label>
                <div class="col-sm-10">
                  <input id="tel" class="form-control" placeholder="请输入电话" type="text">
                </div>
              </div>
              <div class="form-group">
                <label class="col-sm-2 control-label" for="content">内容</label>
                <div class="col-sm-10">
                  <textarea id="content" class="form-control" placeholder="请输入内容" rows="8"></textarea>
                </div>
              </div>
              <div class="form-group">
                <div class="col-sm-offset-2 col-sm-10">
                  <button class="btn btn-default btn-block" type="submit">提交</button>
                </div>
              </div>
            </form>
          </div>
          <!--          <div class="col-xs-12 col-sm-12 col-md-6">-->
          <!--&lt;!&ndash;            <div id="map" class="wow zoomIn"></div>&ndash;&gt;-->
          <!--          </div>-->
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import {WOW} from 'wowjs'
import BMap from "BMap";

export default {
  name: "ContactUs",
  data() {
    return {};
  },
  mounted() {
    var map = new BMap.Map("map"); // 创建地图实例
    // var point = new BMap.Point(116.301841, 40.156506); // 创建点坐标
    // map.centerAndZoom(point, 18); // 初始化地图，设置中心点坐标和地图级别
    // map.enableScrollWheelZoom(true); //开启鼠标滚轮缩放
    // var marker = new BMap.Marker(point); // 创建标注
    // map.addOverlay(marker); // 将标注添加到地图中
    // var opts = {
    //   width: 50, // 信息窗口宽度
    //   height: 10, // 信息窗口高度
    //   title: "黄元公寓" // 信息窗口标题
    // };
    // var infoWindow = new BMap.InfoWindow(
    //   "我的家",
    //   opts
    // ); // 创建信息窗口对象
    map.openInfoWindow(infoWindow, map.getCenter()); // 打开信息窗口
    var wow = new WOW();
    wow.init();
  }
};
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url("../assets/img/banner_1.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}

.ContactUs-container {
  padding: 80px 0;
  transition: all ease 0.5s;
  box-sizing: border-box;
}

#map {
  width: 100%;
  height: 365px;
}

.row {
  margin-right: 0;
  margin-left: 0;
}

@media screen and (max-width: 997px) {
  .ContactUs-container {
    padding: 20px 0;
  }
}
</style>

