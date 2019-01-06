<template>
  <div class="layout">
    <div class="block">
      <el-carousel height="353px">
        <el-carousel-item v-for="item in 4" :key="item">
          <h3>{{ item }}</h3>
        </el-carousel-item>
      </el-carousel>
    </div>

    <div class="nav-list">
      <ul v-for="(item,index) in productList">
        <ul>
          <li v-for="(v,index) in item.list">
            <a href="">{{v.name}}</a>
          </li>
        </ul>
      </ul>
    </div>
    <div class="img-list">
      <ul class="clearfloat">
        <li v-for="listImg in imgList" >
          <router-link :to="listImg.url">
            <img :src="listImg.imgSrc" alt="" class="img-list-size">
            <span class="img-content">{{listImg.content}}</span>
            <span class="img-desc">{{listImg.desc}}</span>
          </router-link>
        </li>
        <!--<li><img src="../assets/list1.jpg" alt=""></li>-->
      </ul>
    </div>

    <div class="pro-list" v-for="more in moreList">
      <div>
        <h3 class="pro-title">{{more.title}}</h3>
        <span class="sub-title">科技改变生活</span>
        <div class="pro-inner">
          <img :src="more.advImg" alt="" class="float-left"/>
          <ul class="clearfloat ul-size">
            <li v-for="pro in more.proImgList" class="float-left pro-size">
              <img :src="pro" alt="">
            </li>
          </ul>
        </div>
      </div>
    </div>
  </div>
</template>


<script>
  export default {
    name: "layout",
    data() {
      return {
        productList: [
          {
            category: '公司简介',
            list: [
              {
                name: "VR眼镜",
                hot: false,
                url: "http://www.by-health.com/about-about"
              },
              {
                name: "无人机",
                hot: true,
                url: "http://www.by-health.com/about-about"
              },
              {
                name: "电动车",
                hot: false,
                url: "http://www.by-health.com/about-about"
              },
              {
                name: "智能手表",
                hot: true,
                url: "http://www.by-health.com/about-about"
              },
              {
                name: "商城动态",
                hot: false,
                url: "http://www.by-health.com/about-about"
              },
              {
                name: "关于我们",
                hot: false,
                url: "http://www.by-health.com/about-about"
              },
            ]
          }
        ],
        imgList: [
          {
            imgSrc: require("../assets/list1.jpg"),
            url: "http://www.123.com",
            content: "科技改变未来",
            desc: "您可以双击这里或者点击编辑按钮来修改内容"
          },
          {
            imgSrc: require("../assets/list2.jpg"),
            url: "http://www.123.com",
            content: "科技改变未来",
            desc: "您可以双击这里或者点击编辑按钮来修改内容"
          },
          {
            imgSrc: require("../assets/list3.jpg"),
            url: "http://www.123.com",
            content: "科技改变未来",
            desc: "您可以双击这里或者点击编辑按钮来修改内容"
          }
        ],
        moreList:[
          {
            title: '四轴航拍无人机',
            advImg: require("../assets/adv1.jpg"),
            proImgList: [
               require("../assets/pro1.jpg"),
               require("../assets/pro2.jpg"),
               require("../assets/pro3.jpg"),
               require("../assets/pro4.jpg"),
               require("../assets/pro5.jpg"),
               require("../assets/pro6.jpg")
            ]
          },
          {
            title: '身临其境的VR体验',
            advImg: require("../assets/adv1.jpg"),
            proImgList: [
               require("../assets/pro1.jpg"),
               require("../assets/pro2.jpg"),
               require("../assets/pro3.jpg"),
               require("../assets/pro4.jpg"),
               require("../assets/pro5.jpg"),
               require("../assets/pro6.jpg")
            ]
          }
        ]
      }
    }
  }
</script>

<style scoped>
  .el-carousel__item h3 {
    color: #475669;
    font-size: 14px;
    opacity: 0.75;
    line-height: 150px;
    margin: 0;
  }

  .el-carousel__item:nth-child(2n) {
    background-color: #1a1a1a;
  }

  .el-carousel__item:nth-child(2n+1) {
    background-color: rgba(117, 117, 117, 0.71);
  }

  .layout {
    position: relative;
    background-color: #f2f2f2;
  }

  .nav-list {
    width: 200px;
    background: #252525;
    z-index: 50;
    position: absolute;
    top: 0;
    height: 353px;
    left: 140px;
  }

  .nav-list li {
    padding: 19px;
    border-bottom: 1px solid #3e3b3b;
    color: #bbbbbb;
    font-size: 15px;
    text-indent: 1em;
  }

  .nav-list li:last-child {
    border: none;
  }

  .img-list {
    width: 100%;
    height: 250px;
    position: relative;
  }

  .img-list ul li {
    float: left;
    margin-right: 11px;
    position: relative;
  }

  .img-list ul li:last-child {
    margin-right: 0;
  }

  .img-list ul {
    width: 80%;
    position: absolute;
    top: 9%;
    left: 10.5%;
  }

  .img-list-size {
    width: 352px;
    height: 200px;
  }

  .img-content{
    position: absolute;
    top: 73px;
    left: 174px;
    color: #000000;
    font-weight: bold;
  }
  .img-desc{
    position: absolute;
    top: 104px;
    left: 175px;
    font-size: 13px;
    letter-spacing: 1px;
    line-height: 23px;
  }
  .pro-list{
    width: 80%;
    margin: 0 auto;
  }
  .pro-title{
    border-left: 4px solid #dd3333;
    padding-left: 8px;
    font-size: 21px;
    font-weight: normal;
    letter-spacing: 1px;
    display: inline-block;
  }
  .sub-title{
    display: inline-block;
    color: #a5a5a5;
    font-size: 13px;
  }
  .pro-inner{
    margin-top: 20px;
    margin-bottom: 40px;
  }
  .ul-size{
    width: 765px;
    margin-left: 332px;
  }
  .pro-size{
    width: 230px;
    height: 280px;
    margin-right: 32px;
    background: white;
    margin-bottom: 36px;
    text-align: center;
  }
  .pro-size:nth-of-type(3n){
    margin-right:0;
  }

</style>
