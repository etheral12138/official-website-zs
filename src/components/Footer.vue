<template>
  <div id="footer" class="container-fluid">
    <div class="logo">
      <img alt="logo图" src="@/assets/img/logo_white.png">
    </div>
    <p class="title">天津智生科技有限公司</p>
    <p class="address_tel_fax">
      <span>地址：公司地址</span>
      <span>Tel：15519701087</span>
    </p>
    <p class="email_wx">
      <span>邮箱：contact@example.com</span>
    </p>
    <p class="copy">Copyright &copy; 2018 - {{ new Date().getFullYear() }} 天津智生科技有限公司</p>
    <!--    <div>-->
    <!--      <p>{{ $t('username') }}</p>-->
    <!--      <p>{{ $t('email') }}</p>-->
    <!--      <p>{{ $t('mobile') }}</p>-->
    <!--    </div>-->
  </div>
</template>
<script>
export default {
  name: "Footer"
};
</script>
<style scoped>
#footer {
  width: 100%;
  height: 100%;
  color: #fff;
  background: #CCB76C;
  overflow: hidden;
  text-align: center;
}

.logo {
  width: 95px;
  height: 45px;
  margin: 50px auto 20px;
}

.title {
  font-size: 25px;
  margin-bottom: 20px;
}

.address_tel_fax {
  color: #d3d3d3;
  font-size: 14px;
  margin: 10px 0;
}

.email_wx {
  color: #d3d3d3;
  font-size: 14px;
}

.copy {
  color: #d3d3d3;
  font-size: 14px;
  margin: 50px 0 10px;
}

@media screen and (max-width: 997px) {
  .title {
    font-size: 20px;
  }

  .address_tel_fax {
    font-size: 12px;
  }

  .email_wx {

    font-size: 12px;
  }

  .copy {
    font-size: 12px;
    margin: 30px 0 10px;
  }
}
</style>

