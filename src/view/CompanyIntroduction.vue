<template>
  <div id="CompanyIntroduction">
    <div class="banner container-fuild text-center">{{ $t('award.award') }}</div>
    <div class="container">
      <div class="row CompanyIntroduction-container">
        <div class="col-xs-12 col-sm-12 col-md-4 wow zoomIn">
          <img class="img-responsive center-block" src="@/assets/img/about_img.png">
        </div>
        <div class="col-xs-12 col-sm-12 col-md-8">
          <!--                    <h3>天津智生科技有限公司</h3>-->
          <!--          <h3>公司研发成员获得荣誉</h3>-->
          <p class=".text-justify"></p>
          <p class=".text-justify"></p>
          <p class=".text-justify">国家级科技一等奖</p>
          国家级科研课题两个
          省级科研课题两个
          <p class=".text-justify">第二届“创祎杯”全国大学生创新创业大赛金奖</p>
          <p class=".text-justify">第二届“创祎杯”全国大学生创新创业大赛铜奖</p>
          <div>
            <a class=".text-justify" href="https://www.sohu.com/a/708231762_121119002">鸿蒙生态星河璀璨丨大学生的开发之路，让初高中几何学习更简单_应用_周文_HarmonyOS
              (sohu.com)</a>
          </div>
          <div>
            <a class=".text-justify" href="http://www.cctime.com/html/2023-8-2/1659049.htm">鸿蒙生态星河璀璨丨机器证明的现实应用，为几何学习“搭桥铺路”
              -- 飞象网 (cctime.com)</a>
          </div>
          <div>
            <a class=".text-justify" href="https://www.163.com/dy/article/IB5C2BDL051189P5.html">鸿蒙生态星河璀璨丨大学生的开发之路，让初高中几何学习更简单|数学|周文|计算机|人工智能_网易订阅
              (163.com)</a>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import {WOW} from 'wowjs';

export default {
  name: 'CompanyIntroduction',
  data() {
    return {}
  },
  mounted() {
    var wow = new WOW();
    wow.init();
  }
}
</script>
<style scoped>
.banner {
  color: #fff;
  font-size: 30px;
  height: 150px;
  line-height: 150px;
  background-image: url('../assets/img/banner1.png');
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}

.row {
  margin-right: 0;
  margin-left: 0;
}

.CompanyIntroduction-container {
  padding: 100px 0;
  color: #808080;
  transition: all ease 0.5s;
}

.CompanyIntroduction-container > div > p {
  font-size: 14px;
  line-height: 2.5rem;
}

@media screen and (max-width: 997px) {
  .CompanyIntroduction-container {
    padding: 10px 0;
    color: #808080;
  }
}
</style>

