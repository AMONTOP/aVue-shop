<template>
  <div id="app">
    <Header></Header>
    <!--<router-view></router-view>-->
    <Layout></Layout>
    <Footer></Footer>
  </div>
</template>

<script>
  import Header from "./components/header"
  import Footer from "./components/footer"
  import Layout from "./components/layout"

  export default {
    name: 'App',
    components: {
      Header,
      Footer,
      Layout
    }
  }
</script>

<style>
  * {
    margin: 0;
    padding: 0;
  }

  ul {
    list-style: none;
  }

  a {
    text-decoration: none;
    color: #666;
  }

  .clearfloat:after {
    display: block;
    clear: both;
    content: "";
    visibility: hidden;
    height: 0
  }

  .clearfloat {
    zoom: 1
  }
  .float-left{
    float: left;
  }
  .float-right{
    float: right;
  }
</style>
