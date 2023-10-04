<template>
  <div id="HomePage">
    <!-- 轮播图 -->
    <div id="swiper" class="container-fuild">
      <div class="swiper-container banner-swiper">
        <div class="swiper-wrapper">
          <div v-for="(item,index) in swiperList" :key="index" class="swiper-slide">
            <img :data-src="item.img" alt="轮播图" class="swiper-lazy">
            <div class="swiper-lazy-preloader"></div>
            <div class="swiper-slide-title">
              <h1>{{ item.title }}</h1>
              <p>{{ item.content }}</p>
            </div>
          </div>
        </div>
        <!-- 如果需要分页器 -->
        <div class="swiper-pagination"></div>

        <!-- 如果需要导航按钮 -->
        <div class="swiper-button-prev"></div>
        <div class="swiper-button-next"></div>
      </div>
    </div>
    <!-- 大数据管理系统 -->
    <div id="bigData" class="container-fuild">
      <div class="row bigData-container">
        <div class="col-xs-12 col-sm-12 col-md-6 wow zoomIn">
          <img alt="" class="img-responsive" src="@/assets/img/img1.png">
        </div>
        <div class="col-xs-12 col-sm-12 col-md-6">
          <h2 class="bigData-title">
            {{ $t('company') }}
            <!--            <small>/ Big Data Management System</small>-->
          </h2>
          <p>
            天津智生科技有限公司，成立于2023年，位于天津市南开区天津大学，是一家以从事计算机、通信和其他电子设备制造业为主的企业。企业目前注册资本60万人民币。公司专注于智慧农业、智慧教育以及智慧医疗三大板块，目前市场验证成功公司项目累计可获得投资3000w以上，市场价值累计达到1亿。
            天津智生科技有限公司拥有10+以上的科研研发团队与20+以上的应用项目开发团队，
            其成员来自清华大学、北京大学、浙江大学、香港中文大学、香港理工大学、香港大学、香港城市大学、天津大学、东南大学、华中科技大学、加拿大多伦多大学、英国剑桥大学、中国人工智能协会、江苏省人工智能协会、中国图像图形学会、美国加州大学、新加坡国立大学等100多家国内外高校的博士、研究生等，在科研项目研发上由中国博士后联盟进行指导，
            公司研发人员累计200名以上，战略合作伙伴100+家。</p>
          <!--          <h2 class="bigData-device">PC/PAD/Phone &nbsp; 全设备支持</h2>-->
          <!--          <a class="btn btn-lg btn-block btn-info" href="#">联系我们</a>-->
        </div>
      </div>
    </div>
    <!-- 主营业务 -->
    <div id="contactUs" class="container-fuild text-center">
      <div class="container contactUs-container wow slideInUp">
        <h1>{{ $t('main') }}</h1>
        <p>
          一般项目：技术服务、技术开发、技术咨询、技术交流、技术转让、技术推广；人工智能双创服务平台；互联网数据服务；人工智能基础资源与技术平台；人工智能公共数据平台；人工智能通用应用系统；人工智能行业应用系统集成服务；信息系统集成服务；人工智能硬件销售；人工智能公共服务平台技术咨询服务；软件开发；计算机系统服务；人工智能应用软件开发；人工智能基础软件开发；人工智能理论与算法软件开发；平面设计；数据处理服务；网络与信息安全软件开发；数据处理和存储支持服务；计算机软硬件及辅助设备零售；计算机软硬件及辅助设备批发；工业控制计算机及系统销售，科技课题研发。</p>
        <!--        <button-->
        <!--          class="btn btn-default btn-sm"-->
        <!--          onmouseenter="this.style.backgroundColor='transparent'; this.style.borderColor='#ffffff'; this.style.color='#ffffff';"-->
        <!--          onmouseleave="this.style.borderColor='#ffffff'; this.style.backgroundColor='#ffffff'; this.style.color='#3f3f3f';"-->
        <!--        >联系我们-->
        <!--        </button>-->
        <!--        <div class="contactUs-contactWay">-->
        <!--          <span></span>-->
        <!--          <span></span>-->
        <!--          <span></span>-->
        <!--        </div>-->
      </div>
    </div>
    <!-- 客户评价 -->
    <!--    <div id="customer" class="container-fuild">-->
    <!--      <div class="container customer-container">-->
    <!--        <p class="customer-title text-center">团队介绍</p>-->
    <!--        <div class="swiper-container customer-swiper hidden-xs">-->
    <!--          <div class="swiper-wrapper">-->
    <!--            <div-->
    <!--              class="swiper-slide customer-block"-->
    <!--              v-for="(item,index) in customerList"-->
    <!--              :key="index"-->
    <!--            >-->
    <!--              <div class="customer-logo">-->
    <!--                <img class="center-block" :src="item.logo" alt="logo">-->
    <!--              </div>-->
    <!--              <div class="customer-yh">-->
    <!--                <img src="@/assets/img/yinhao.png" alt="引号">-->
    <!--              </div>-->
    <!--              <div class="customer-content1">-->
    <!--                <small>{{item.content}}</small>-->
    <!--              </div>-->
    <!--              <div class="customer-content2">{{item.title}}</div>-->
    <!--            </div>-->
    <!--          </div>-->
    <!--          &lt;!&ndash; 如果需要导航按钮 &ndash;&gt;-->
    <!--          <div class="swiper-button-prev"></div>-->
    <!--          <div class="swiper-button-next"></div>-->
    <!--        </div>-->
    <!--        <div class="row visible-xs customer-block">-->
    <!--          <div class="col-xs-16" v-for="(item,index) in customerList" :key="index">-->
    <!--            <div class="customer-logo">-->
    <!--              <img class="center-block" :src="item.logo" alt="logo">-->
    <!--            </div>-->
    <!--            <div class="customer-yh">-->
    <!--              <img src="@/assets/img/yinhao.png" alt="引号">-->
    <!--            </div>-->
    <!--            <div v-html="item.content" class="customer-content1">-->
    <!--            </div>-->
    <!--            <div class="customer-content2">-->
    <!--              <small>{{item.title}}</small>-->
    <!--            </div>-->
    <!--          </div>-->
    <!--        </div>-->
    <!--      </div>-->
    <!--    </div>-->
    <!-- 为什么选择我们 -->
    <div id="whyChooseUs" class="conatiner-fuild">
      <div class="container text-center">
        <div class="whyChooseUs-title text-center">
          <p>{{ $t('group') }}</p>
          <!--          <p>THE REASON TO CHOOSING US</p>-->
        </div>
        <div class="row row-cols-4">
          <div
            v-for="(item,index) in serverList"
            :key="index"
            class=" col  server-wrapper"
          >
            <div
              class="server-block wow slideInUp">
              <!--              onmouseenter="this.style.color='#28f';this.style.borderColor='#28f'"-->
              <!--              onmouseleave="this.style.color='#666';this.style.borderColor='#ccc'"-->
              <div>
                <img :src="item.logo" alt="logo" class="center-block img-circle">
              </div>
              <div>
                <p class="text-center">{{ item.title }}</p>
                <div
                  class="text-center"
                  v-html="item.content">
                  <!--                  onmouseenter="this.style.color='#28f'"-->
                  <!--                  onmouseleave="this.style.color='#ccc'"-->
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import Swiper from "swiper";
import {WOW} from 'wowjs';

export default {
  name: "HomePage",
  data() {
    return {
      swiperList: [
        {
          img: require("@/assets/img/banner1.png"),
          path: "",
          title: '基于细粒度图像分类与特征识别的人眼疾病自动分析与诊断研究',
          content: '眼科学是医学领域的难点和重点,影像诊断是一种眼科疾病干预和检测手段，本研究基于计算机视觉技术来进行人眼疾病自动分析与诊断研究，旨在提高人们对眼疾病的早期检测和诊断的准确性，从而减轻患者的痛苦和提高治疗的成功率。',
        },
        {
          img: require("@/assets/img/banner2.jpg"),
          path: "",
          title: '计算机视觉中的小目标的快速检测',
          content: '小目标检测是计算机视觉领域中的重难点，精准度差、样本少等问题使小目标检测成为一大难题。本项目拟将更多的小目标样本进行训练并改进相关算法同时在原有基础之上创建更精准的算法。利用YOLO等框架和神经网络模型，提升更为复杂的情况下的小目标检测的精准度。',
        },
        {
          img: require("@/assets/img/banner1.png"),
          path: "",
          title: '智慧医疗',
          content: '基于细粒度图像分类与特征识别的人眼疾病自动分析与诊断研究：江苏省省级科研项目,基于启发式特征搜索与集合深度学习的阿尔茨海默病的自动诊断分析与病理机制研究：江苏省国家级科研项目',
        }
        // {
        //   img: require("@/assets/img/banner2.jpg"),
        //   path: "",
        //   title: '您身边的IT专家4',
        //   content: '宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介宣传简介',
        // }
      ],
      // customerList: [
      //   {
      //     logo: require("@/assets/img/fys.png"),
      //     title:
      //       "范雨生",
      //     content:
      //       "天津智生科技有限公司CEO\n" +
      //       "主要研究方向为计算机视觉方向\n" +
      //       "拥有强大的算法工程师团队（20余人）\n" +
      //       "软件开发团队（10余人）\n" +
      //       "南京驰软科技有限公司特邀执行监事\n" +
      //       "香港中文大学PHD\n" +
      //       "曾获得悉尼大学、香港中文大学、香港理工、\n" +
      //       "哥伦比亚大学研究生offer\n" +
      //       "发表学术论文累计10余篇\n" +
      //       "获得奇迹投资、C2C东禾智创等投资者认可，目前可获得市场融资600w以上\n" +
      //       "自承接科技项目市场价值累计达到6000w(金银花采摘、水果采摘、农业采摘、智慧农业产业)\n" +
      //       "多家互联网加大厂产品经理获得者"
      //   },
      //   {
      //     logo: require("@/assets/img/zdb.png"),
      //     title:
      //       "张东波",
      //     content:
      //       "博士生导师，2007年 获得湖南大学控制科学与工程博士学位，1996年起在自动化与电子信息学院从教至今，主要从事机器视觉、智能机器人等相关研究，发表过机器人领域顶刊，主持过广东省基础与应用基础研究基金联合基金重点项目“智能机器人自主视知觉计算模型与原型系统研究”。"
      //   },
      //   {
      //     logo: require("@/assets/img/wly.png"),
      //     title:
      //       "魏雷远",
      //     content:
      //       ""
      //   },
      //   {
      //     logo: require("@/assets/img/zw.png"),
      //     title:
      //       "周文",
      //     content: ""
      //     // "<p>2022年参加江苏省某医疗项目(金山估值初期2000w)，获得过多家企业offer。</p>"+
      //     // "<p>大学期间获得了江苏省大学生创新创业训练计划国家级创新项目(第二主持人+核心技术骨干&负责人)、国家级课题一个(主持 人工智能在游戏中的对应策略)、IEER一等奖、数维杯国际赛（H）、联合国采购杯一等奖、国家科技一等奖、服务外包创新创业区域三等奖、KAGGLE银牌、百度之星省级一等奖等多个省级以上的奖项</p>" +
      //     // "<p>担任多个互联网加省级奖项以上团队的技术总监。</p>" +
      //     // "<p>第二届“创祎杯”全国大学生创新创业大赛 金奖。</p>" +
      //     // "<p>发表学术论文累计16篇,包含SCI(JCR一区、二区等)、EI期刊/会议论文等,目前跟随新加坡新国立大学助理教授开展AI+疾病识别方向的课题。</p>" +
      //     // "<p>获得实用型专利两个、计算机著作权五个</p>" +
      //     // "<p>2023打磨国家级创新创业训练项目一个、省级创新创业训练项目一个.2022辅导结项省级创新创业项目一个。</p>" +
      //     // "<p>自承接计算机商业项目两个及以上(藏品开发、自动扫码洗车等，市场价值达20w以上)。</p>" +
      //     // "<p>Retry团队创始人</p>" +
      //     // "<p>获得华为与中国新闻周刊的联合采访和报道。</p>"
      //   },
      // ],
      serverList: [
        {
          logo: require("@/assets/img/fys.png"),
          title: "范雨生",
          content: "<p>天津智生科技有限公司CEO，</p>" +
            "<p>主要研究方向为计算机视觉方向,拥有强大的算法工程师团队（20余人），软件开发团队（10余人），</p>" +
            "<p>南京驰软科技有限公司特邀执行监事，</p>" +
            "<p>香港中文大学PHD,曾获得悉尼大学、香港中文大学、香港理工、哥伦比亚大学研究生offer,发表学术论文累计10余篇，</p>" +
            "<p>获得奇迹投资、C2C东禾智创等投资者认可，目前可获得市场融资600w以上，</p>" +
            "<p>自承接科技项目市场价值累计达到6000w(金银花采摘、水果采摘、农业采摘、智慧农业产业)，</p>" +
            "<p>多家互联网加大厂产品经理获得者</p>"
        },
        {
          logo: require("@/assets/img/zdb.png"),
          title: "张东波",
          content: "<p>博士生导师，</p>" +
            "<p>2007年 获得湖南大学控制科学与工程博士学位，1996年起在自动化与电子信息学院从教至今，</p>" +
            "<p>1996年起在自动化与电子信息学院从教至今，主要从事机器视觉、智能机器人等相关研究，</p>" +
            "<p>主要从事机器视觉、智能机器人等相关研究，发表过机器人领域顶刊，主持过广东省基础与应用基础研究基金联合基金重点项目“智能机器人自主视知觉计算模型与原型系统研究”。</p>"
        },
        {
          logo: require("@/assets/img/wly.png"),
          title: "魏雷远",
          content: "<p>中国电工技术学会高级会员、能源智慧化专委会委员，北京市职称评审专家库成员，</p>" +
            "<p>高级工程师（电力）、注册电气工程师（发输变电专业执业资格）、高级项目经理（系统集成）、系统分析师、信息系统项目管理师，</p>" +
            "<p>北京华信易成科技有限公司总经理</p>"
        },
        {
          logo: require("@/assets/img/zw.png"),
          title: "周文",
          content: "<p>2022年参加江苏省某医疗项目(金山估值初期2000w)，获得过多家企业offer。</p>" +
            "<p>大学期间获得了江苏省大学生创新创业训练计划国家级创新项目(第二主持人+核心技术骨干&负责人)、国家级课题一个(主持 人工智能在游戏中的对应策略)、IEER一等奖、数维杯国际赛（H）、联合国采购杯一等奖、国家科技一等奖、服务外包创新创业区域三等奖、KAGGLE银牌、百度之星省级一等奖等多个省级以上的奖项</p>" +
            "<p>担任多个互联网加省级奖项以上团队的技术总监。</p>" +
            "<p>第二届“创祎杯”全国大学生创新创业大赛 金奖。</p>" +
            "<p>发表学术论文累计16篇,包含SCI(JCR一区、二区等)、EI期刊/会议论文等,目前跟随新加坡新国立大学助理教授开展AI+疾病识别方向的课题。</p>" +
            "<p>获得实用型专利两个、计算机著作权五个</p>" +
            "<p>2023打磨国家级创新创业训练项目一个、省级创新创业训练项目一个.2022辅导结项省级创新创业项目一个。</p>" +
            "<p>自承接计算机商业项目两个及以上(藏品开发、自动扫码洗车等，市场价值达20w以上)。</p>" +
            "<p>Retry团队创始人。</p>" +
            "<p>获得华为与中国新闻周刊的联合采访和报道。</p>"
        }
      ]
    };
  },
  mounted() {
    /* banner-swiper */
    new Swiper(".banner-swiper", {
      loop: true, // 循环模式选项
      effect: 'fade',
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要分页器
      pagination: {
        el: ".swiper-pagination",
        clickable: true
      },
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },
      // 延迟加载
      lazy: {
        loadPrevNext: true
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });
    /* customer-swiper */
    new Swiper(".customer-swiper", {
      loop: true, // 循环模式选项
      slidesPerView: 3,
      //自动播放
      autoplay: {
        delay: 3000,
        stopOnLastSlide: false,
        disableOnInteraction: false
      },
      // 如果需要前进后退按钮
      navigation: {
        nextEl: ".swiper-button-next",
        prevEl: ".swiper-button-prev"
      },
      observer: true, //修改swiper自己或子元素时，自动初始化swiper
      observeParents: true //修改swiper的父元素时，自动初始化swiper
    });
    /* wowjs动画 */
    var wow = new WOW({
      boxClass: 'wow',
      animateClass: 'animated',
      offset: 0,
      mobile: true,
      live: true
    })
    wow.init();
  }
};
</script>
<style scoped>
/* 整体盒子 */
#HomePage {
  width: 100%;
}

/* 轮播图 */
#swiper {
  height: 600px;
}

#swiper .banner-swiper {
  width: 100%;
  height: 100%;
}

#swiper .banner-swiper .swiper-slide img {
  width: 100%;
  height: 100%;
}

#swiper .banner-swiper .swiper-slide {
  position: relative;
}

#swiper .banner-swiper .swiper-slide-title {
  position: absolute;
  top: 0;
  left: 0;
  z-index: 999999999;
  width: 100%;
  height: 100%;
  color: #fff;
  background: rgba(51, 51, 51, 0.534);
  text-align: center;
  line-height: 80px;
}

#swiper .banner-swiper .swiper-slide-title > h1 {
  font-size: 50px;
  margin-top: 12%;
}

#swiper .banner-swiper .swiper-slide-title > p {
  font-size: 20px;
  margin-top: 1%;
  font-weight: 700;
}

/* 大数据管理系统 */
#bigData {
  padding: 100px;
  transition: all ease 0.6s;
  box-sizing: border-box;
}

#bigData .bigData-title {
  padding-bottom: 10px;
  border-bottom: 1px solid #ccc;
}

#bigData p {
  font-size: 14px;
  color: #333;
  line-height: 2rem;
}

#bigData .bigData-device {
  margin: 50px 0 20px;
}

/* 您身边的IT专家 */
#contactUs {
  color: #fff;
  height: 400px;
  background: url("../assets/img/contact_us_bg.jpg") 0 0 no-repeat;
  background-size: 100% 100%;
  transition: all ease 0.6s;
}

#contactUs .contactUs-container {
  padding-top: 50px;
}

#contactUs .contactUs-container button {
  width: 300px;
  height: 50px;
  margin-top: 40px;
}

#contactUs .contactUs-container .contactUs-contactWay span {
  display: inline-block;
  width: 48px;
  height: 48px;
  margin: 30px;
}

#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(1) {
  background: url("../assets/img/weixin.png") 0 0 no-repeat;
  background-size: 100% 100%;
}

#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(2) {
  background: url("../assets/img/weibo.png") 0 0 no-repeat;
  background-size: 100% 100%;
}

#contactUs .contactUs-container .contactUs-contactWay span:nth-of-type(3) {
  background: url("../assets/img/twitter.png") 0 0 no-repeat;
  background-size: 100% 100%;
}

/* 客户评价 */
#customer {
  padding: 50px 0;
  box-sizing: border-box;
  background: #efefef;
  transition: all ease 0.6s;
}

#customer .customer-title {
  font-size: 30px;
  color: rgb(102, 102, 102);
  margin: 0 0 30px;
}

#customer .customer-block {
  background: #fff;
  padding: 30px;
}

#customer .customer-logo img {
  width: 94px;
  height: 94px;
  border: 1px solid #ccc;
}

#customer .customer-yh img {
  width: 34px;
  height: 34px;
}

#customer .customer-content1 {
  padding-bottom: 20px;
  border-bottom: 1px solid #0ce9f1;
}

#customer .customer-content2 {
  padding-top: 20px;
}

/* 为什么选择我们 */
#whyChooseUs {
  padding: 100px;
}

#whyChooseUs .whyChooseUs-title {
  margin-bottom: 50px;
}

#whyChooseUs .whyChooseUs-title p:nth-of-type(1) {
  font-size: 25px;
  font-weight: 500;
}

#whyChooseUs .whyChooseUs-title p:nth-of-type(2) {
  font-size: 14px;
}

#whyChooseUs .server-block {
  padding: 50px 20px;
  border: 1px solid #ccc;
  border-bottom: 5px solid #ccc;
//display: flex;
}

#whyChooseUs .server-block img {
  width: 10rem;
  height: 10rem;
}

#whyChooseUs .server-block > p {
  font-size: 20px;
  margin: 30px 0;
}

#whyChooseUs .server-block > div {
  color: #000;
}

/* 媒体查询（手机） */
@media screen and (max-width: 768px) {
  #swiper {
    height: 200px;
  }

  #bigData {
    padding: 30px;
  }

  #bigData .bigData-title {
    font-size: 20px;
  }

  #bigData .bigData-device {
    font-size: 20px;
    margin: 10px 0 10px;
  }

  #contactUs {
    height: 200px;
    transition: all ease 0.6s;
  }

  #contactUs .contactUs-container {
    padding-top: 0;
  }

  #contactUs .contactUs-container h1 {
    font-size: 25px;
  }

  #contactUs .contactUs-container h3 {
    font-size: 18px;
  }

  #contactUs .contactUs-container button {
    width: 200px;
    height: 30px;
    margin-top: 20px;
  }

  #contactUs .contactUs-container .contactUs-contactWay span {
    display: inline-block;
    width: 28px;
    height: 28px;
    margin: 10px;
  }

  #customer {
    padding: 30px 0;
    box-sizing: border-box;
    background: #fff;
  }

  #customer .customer-title {
    font-size: 16px;
    font-weight: bold;
  }

  #customer .customer-logo img {
    width: 48px;
    height: 48px;
  }

  #customer .customer-block {
    padding: 30px;
  }

  #customer .customer-block > div {
    padding: 30px 0;
  }

  #whyChooseUs {
    padding: 20px 0;
    transition: all ease 0.6s;
  }

  #whyChooseUs .whyChooseUs-title p:nth-of-type(1) {
    font-size: 20px;
    font-weight: 700;
  }

  #whyChooseUs .whyChooseUs-title p:nth-of-type(2) {
    font-size: 12px;
  }

  #whyChooseUs .server-block {
    padding: 50px 0;
    border: 1px solid #ccc;
    border-bottom: 5px solid #ccc;
  }

  #whyChooseUs .server-block img {
    width: 10rem /* 6/16 */;
    height: 10rem;
  }

  #whyChooseUs .server-block > p {
    font-size: 20px;
    margin: 20px 0;
  }

  #whyChooseUs .server-block > div {
    color: #000;
  }
}

/* 媒体查询（平板） */
@media screen and (min-width: 768px) and (max-width: 996px) {
  #swiper {
    height: 400px;
  }

  #bigData {
    padding: 60px;
  }

  #bigData .bigData-title {
    font-size: 30px;
  }

  #bigData .bigData-device {
    font-size: 30px;
    margin: 30px 0 15px;
  }

  #contactUs {
    height: 300px;
  }

  #contactUs .contactUs-container {
    padding-top: 50px;
  }

  #contactUs .contactUs-container h1 {
    font-size: 30px;
  }

  #contactUs .contactUs-container h3 {
    font-size: 20px;
  }

  #contactUs .contactUs-container button {
    width: 300px;
    height: 50px;
    margin-top: 30px;
  }

  #contactUs .contactUs-container .contactUs-contactWay span {
    display: inline-block;
    width: 32px;
    height: 32px;
    margin: 15px;
  }

  #customer .customer-title {
    font-size: 24px;
  }

  #whyChooseUs {
    padding: 20px 0;
  }
}
</style>

