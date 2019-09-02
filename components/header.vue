<template>
  <div class="container">
    <el-row type="flex" class="main" justify="space-between">
      <div class="logo">
        <nuxt-link to="/">
          <img src="http://157.122.54.189:9093/images/logo.jpg" alt />
        </nuxt-link>
      </div>
      <el-row type="flex" class="navs">
        <!-- <nuxt-link></nuxt-link>的使用方式和作用和<router-link></router-link>相同 -->
        <nuxt-link to="/">首页</nuxt-link>
        <nuxt-link to="/post/indexPost">旅游攻略</nuxt-link>
        <nuxt-link to="/hotel/indexHotel">酒店</nuxt-link>
        <nuxt-link to="/air/indexAir">国内机票</nuxt-link>
      </el-row>

      <!-- 登录/跳转 -->
      <div class="login">
        <el-dropdown class="el-dropdown">
          <span class="el-dropdown-link">
              <i class="el-icon-bell "></i>
            消息
            <i class="el-icon-caret-bottom "></i>
          </span>
          <el-dropdown-menu slot="dropdown">
            <el-dropdown-item>消息</el-dropdown-item>
            
          </el-dropdown-menu>
        </el-dropdown>
        
        <nuxt-link to="/user/login"> 登录/注册</nuxt-link>
      </div>
    </el-row>
  </div>
</template>

<script>
export default {};
</script>

<style lang='less' scoped>
.container {
  height: 60px;
  line-height: 60px;
  background: #fff;
  border-bottom: 1px solid #ddd;
  box-shadow: 0 3px 0 #f5f5f5;
  box-sizing: border-box;
}
.main {
  width: 1000px;
  margin: 0 auto;
}

.navs {
  flex: 1;
  margin-left: 10px;
  a {
    display: block;
    height: 60px; //居中
    padding: 0 20px;
    box-sizing: border-box;

    &:hover {
      color: #409eff;
      border-bottom: 5px #409eff solid;
    }
  }

  .nuxt-link-exact-active {
    background: #409eff;
    color: #fff;

    &:hover {
      color: #fff;
    }
  }
}

.logo {
  padding-top: 9px;
  img {
    width: 156px;
    height: 42px;
    display: block;
  }
}
.el-dropdown{
    margin-right: 16px;
}
.el-dropdown-link{
    cursor: pointer;
    color:#606266;
    font-style: 14px;
}

</style>