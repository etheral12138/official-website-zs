<template>
  <div id="ServiceDetail">
    <div class="banner container-fuild text-center">专注行业</div>
    <div class="container">
      <div class="row">
        <div id="myScrollspy" class="col-xs-12 col-sm-12 col-md-3">
          <ul id="myNav" class="nav nav-tabs nav-stacked center-block">
            <p>目录</p>
            <li
              v-for="(item,index) in serviceNavList"
              :key="index"
              :class="item.id===id?'active':''"
            >
              <a :href="'#'+item.id">{{ item.title }}</a>
            </li>
          </ul>
        </div>
        <div class="col-xs-12 col-sm-12 col-md-9 content  wow zoomIn">
          <div v-for="(item,index) in serviceContentList" :key="index" class="content-block">
            <h2 :id="item.id">
              {{ item.title }}
              <small>/ {{ item.eng_title }}</small>
            </h2>
            <div v-html="item.content"></div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
import {WOW} from "wowjs";

export default {
  name: "ServiceDetail",
  data() {
    return {
      id: "section-1",
      serviceNavList: [
        {
          id: "section-1",
          title: "智慧农业"
        },
        {
          id: "section-2",
          title: "智慧教育"
        },
        {
          id: "section-3",
          title: "智慧医疗"
        },
        // {
        //   id: "section-4",
        //   title: "iOS应用定制开发"
        // }
      ],
      serviceContentList: [
        {
          id: "section-1",
          title: "智慧农业",
          eng_title: "Smart Agriculture",
          content:
            "<h3>金银花采摘机器人</h3>" +
            "<p>简介:金银花采摘一体化机器人是一种可自动化执行金银花采摘任务的智能机器人。它具备识别金银花植株、定位可采摘的花朵以及进行精准采摘等功能。金银花采摘一体化机器人的引入可以提高采摘效率、降低人力成本，并且在大规模种植金银花的农场中特别有用。它能够快速准确地采摘花朵，提高生产效率，同时减少了人工劳动的繁重程度。此外，机器人在采摘过程中还可以收集相关数据，为农场的种植管理提供参考和支持，进一步优化农作物的生长和品质。</p>" +
            "<p>项目级别:目前项目市场价值预计5000w。</p>" +
            "<h3>火龙果采摘机器人</h3>" +
            "<p>简介: 火龙果采摘一体化机器人是一种可自动化执行金银花采摘任务的智能机器人。它具备识别火龙果、定位可采摘的火龙果以及进行精准采摘等功能。火龙果采摘一体化机器人的引入可以提高采摘效率、降低人力成本，并且在大规模种植火龙果的农场中特别有用。它能够快速准确地采摘火龙果，提高生产效率，同时减少了人工劳动的繁重程度。此外，机器人在采摘过程中还可以收集相关数据，为农场的种植管理提供参考和支持，进一步优化农作物的生长和品质。</p>" +
            "<p>项目级别:已获得50w投资，市场价值预计4000w。</p>"
        },
        {
          id: "section-2",
          title: "智慧教育",
          eng_title: "Smart Education",
          content:
            "<h3>优途优选-大学生一体化职业规划平台(国内首家大学生专业平台)</h3>" +
            "<p>简介: 优途优选，是一个以围绕大学生核心竞争力成长和职业规划为中心的教育服务类企业。项目旨在根据学生自身的专业特点、性格特点、职业爱好，订制个性化的职业规划，在学生在校期间实时跟踪学生的学业表现和核心竞争力的变化，打造大学生在校期间个人成长的一站式平台。本平台即旨在激发和挖掘学生的学术潜力和专业学习潜力，帮助学生更加快速和科学地成长。同时，我们根据学生的职业发展实时动态变化和学生的意向，接入有实力的、合适的企业来平台对有意向实习和工作的同学进行人才招聘。</p>" +
            "<p>市场价值:预计3000w</p>" +
            "<h3>Newclass-你会喜欢的智慧教室(第二届“创祎杯”全国大学生创新创业大赛金奖)</h3>" +
            "<p>简介: NewClass 智慧教室倡导“传播智慧和尊重”的教育理念，致力于把智慧和健康带给全球亿万师生和用户，以更前沿的视野聚焦教育，助力信息化教育的发展。产品主要包括乐涂、智慧创客互动教室、录播直播教室、慕课王、校园智能综合管理系统等用于学前教室、高校、企业会议室、展厅、教育培训等场所，实现智能书写、演示、常态化录直播、课堂以及远程交互、校园智能管理等功能。\n" +
            "项目荣誉: 第二届“创祎杯”全国大学生创新创业大赛金奖。</p>" +
            "<p>市场价值: 预计1000w。</p>"
        },
        {
          id: "section-3",
          title: "智慧医疗",
          eng_title: "Smart Medical",
          content:
            "<h3>基于细粒度图像分类与特征识别的人眼疾病自动分析与诊断研究：江苏省省级科研项目（项目内部技术资料保密)</h3>" +
            "<p>简介:眼科学是医学领域的难点和重点,影像诊断是一种眼科疾病干预和检测手段，本研究基于计算机视觉技术来进行人眼疾病自动分析与诊断研究，旨在提高人们对眼疾病的早期检测和诊断的准确性，从而减轻患者的痛苦和提高治疗的成功率。</p>" +
            "<h3>这是标题2</h3>" +
            "<p>简介: 阿尔茨海默病是当今世界面临的最严重的神经退行性疾病之一，目前还没有有效的治疗AD的方法，本项目主要基于特征搜索和人工智能中的深度学习技术来研究阿尔茨海默病的病理机制以及阿尔茨海默病的医学影像的自动快速诊断分析。 </p>"
        },
        // {
        //   id: "section-4",
        //   title: "iOS应用定制开发",
        //   eng_title: "iOS App Dev",
        //   content:
        //     "<h3>这是标题1</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p><h3>这是标题2</h3><p>这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。这里是内容，请根据实际需要修改。</p>"
        // }
      ]
    };
  },
  mounted() {
    this.id = this.$route.params.id;
    var top = document.getElementById(this.id).offsetTop;
    $(window).scrollTop(top + 300);
    $("#myNav").affix({
      offset: {
        top: 300
      }
    });
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
  background-image: url("../assets/img/banner_2.jpg");
  background-repeat: no-repeat;
  background-size: cover;
  background-attachment: scroll;
  background-position: center center;
}

ul.nav-tabs {
  width: 200px;
  margin-top: 40px;
  border-radius: 4px;
  background: #fff;
  z-index: 99999;
  border: 1px solid #474747;
  box-shadow: 0 1px 4px rgba(0, 0, 0, 0.067);
}

ul.nav-tabs li {
  text-align: center;
  margin: 0;
  border-top: 1px solid #474747;
}

ul.nav-tabs p {
  color: #fff;
  font-size: 18px;
  font-weight: bold;
  text-align: center;
  background: #474747;
  margin: 0;
  padding: 10px 0;
}

ul.nav-tabs li:first-child {
  border-top: none;
}

ul.nav-tabs li a {
  margin: 0;
  padding: 8px 16px;
  border-radius: 0;
}

ul.nav-tabs li.active a,
ul.nav-tabs li.active a:hover {
  color: #fff;
  background: #474747;
  border: 1px solid #474747;
}

ul.nav-tabs li:first-child a {
  border-radius: 4px 4px 0 0;
}

ul.nav-tabs li:last-child a {
  border-radius: 0 0 4px 4px;
}

ul.nav-tabs.affix {
  top: 30px;
}

.content-block {
  margin: 50px 0;
}

.content-block > h2 {
  padding: 20px 0;
  border-bottom: 1px solid #ccc;
}
</style>
