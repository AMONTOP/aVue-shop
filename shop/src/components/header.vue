<template>
  <div class="app-head">
    <div class="app-head-inner">
      <div style="width: 80%;margin: 0 auto">
        <span>在线时间 08:30~21:30  欢迎访问家用设备在线商城！</span>
        <ul class="head-ul">
          <li>登录</li>
          <li>|</li>
          <li>注册</li>
          <li><img src="" alt=""></li>
        </ul>
      </div>
    </div>
    <div class="app-head-nav">

      <img class="logo-img" src="../assets/logo.png" alt="">
      <ul>
        <li>首页</li>
        <li>所有商品</li>
        <li>商城动态</li>
        <li>关于我们</li>
        <li>线下门店</li>
        <li>
          <input class="enter-key" type="text" placeholder="输入关键字">
          <a href="" class="submit-a"></a>
        </li>
      </ul>

    </div>
  </div>
</template>

<script>
    export default {
        name: "header"
    }
</script>

<style scoped>
.app-head{
  width: 100%;
}
.app-head-inner{
  width: 100%;
  height: 46px;
  line-height: 46px;
  margin: 0 auto;
  color: #dddddd;
  font-size: 13px;
  background: #757575;
}
.head-ul{
  display: inline-block;
  float: right;
}
.head-ul li{
  float: left;
  margin-left: 10px;
}
.app-head-nav{
  width: 80%;
  margin: 0 auto;
  height: 98px;
  line-height:98px;
}
.logo-img{
  width: 251px;
  vertical-align: top;
  margin-top: 22px;
}
.app-head-nav ul{
  display: inline-block;
  width: 76%;
  height: 98px;
}
.app-head-nav ul li{
  float: left;
  margin-left: 40px;
  color: #777777;
  font-size: 14px;
}
.app-head-nav ul li:last-child{
  margin-left: 80px;
  position: relative;
}
  .enter-key{
    width: 262px;
    height: 37px;
    text-indent: 1em;
    position: relative;
  }

  .submit-a {
    background: #dd3333 none repeat scroll 0 0;
    cursor: pointer;
    height: 40px;
    width: 40px;
    position: absolute;
    top: 29px;
    right: 0;
  }
</style>
