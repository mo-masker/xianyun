<template>
  <div class="container">
    <el-row type="flex" justify="space-between" class="main">
      <!-- logo -->
      <div class="logo">
        <nuxt-link to="/">
          <img src="http://157.122.54.189:9093/images/logo.jpg" alt>
        </nuxt-link>
      </div>
      <!-- 菜单 -->
      <el-row type="flex" class="navs">
        <nuxt-link to="/">
          首页
        </nuxt-link>
        <nuxt-link to="post">
          旅游攻略
        </nuxt-link>
        <nuxt-link to="hotel">
          酒店
        </nuxt-link>
        <nuxt-link to="air">
          机票
        </nuxt-link>
      </el-row>
      <!-- 右侧的登录注册 -->
      <div>
        <!-- v-if 是判断是否显示 -->
        <div v-if="false">
          <nuxt-link to="/user/login">
            登录注册
          </nuxt-link>
        </div>
        <el-dropdown>
          <el-dropdown>
            <span class="el-dropdown-link">
              <img src="http://157.122.54.189:9095/assets/images/avatar.jpg" alt>
              团灭发动机
              <i class="el-icon-arrow-down el-icon--right" />
            </span>
            <el-dropdown-menu slot="dropdown">
              <el-dropdown-item>个人中心</el-dropdown-item>
              <el-dropdown-item>退出</el-dropdown-item>
            </el-dropdown-menu>
          </el-dropdown>
        </el-dropdown>
      </div>
    </el-row>
  </div>
</template>

<script>
export default {}
</script>

<style lang="less" scoped>
// 设置阴影
.container {
  box-shadow: 0 2px 2px #ddd;
}
.main {
  width: 1000px;
  height: 60px;
  // border: 2px solid blue;
  margin: 0 auto;
  line-height: 60px;
}
.logo {
  margin-right: 20px;
  img {
    width: 156px;
    height: 42px;
    margin-top: 9px;
  }
}

.navs {
  flex: 1;

  a {
    display: block;
    padding: 0 20px;
    height: 60px;
    // 内减
    box-sizing: border-box;

    &:hover {
      color: #409eff;
      // 下划线
      border-bottom: 5px #409eff solid;
    }
  }
  .nuxt-link-exact-active {
    background-color: #409eff;
    color: #fff;

    &:hover {
      color: #fff;
    }
  }
}

.el-dropdown-link{
  img{
    width: 36px;
    height: 36px;
    // 居中
    vertical-align: middle;
  }
}
</style>
