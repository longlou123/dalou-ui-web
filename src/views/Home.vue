<template>
  <div class="home">
    <top-nav></top-nav>
    <div class="content">
      <h1>Vue UI框架</h1>
      <h2>此UI框架仅为个人学习参考使用，欢迎交流。</h2>
      <div class="btnv">
        <a target="_blank" href="" class="git">博客</a>
        <a target="_blank" href="" class="git">GitHub</a>
        <router-link to="/doc/switch">开始</router-link>
      </div>
    </div>
    <div class="desc">
      <div class="item">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-Vue"></use>
        </svg>
        <div>
          <div class="title">基于Vue</div>
          <div class="d-x">使用了Vue全家桶</div>
        </div>
      </div>
      <div class="item">
        <img class="img-box" src="data:image/png;base64,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" alt="xxx">
        <!-- <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-typescript"></use>
        </svg> -->
        <div>
          <div class="title">基于JavaScript</div>
          <div class="d-x">源代码采用JavaScript书写</div>
        </div>
      </div>
      <div class="item">
        <svg class="icon" aria-hidden="true">
          <use xlink:href="#icon-tubiao06"></use>
        </svg>
        <div>
          <div class="title">代码易读</div>
          <div class="d-x">每个组件的源代码都极其简洁</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import TopNav from '../components/TopNav.vue';
export default {
  name:'home',
  components: {TopNav},
}
</script>

<style lang="scss" scoped>
$h1_color: #1E90FF;
$bg: #1E90FF;
$btn_color: #fff;
$border_radius: 4px;
.home {
  ::v-deep(.top-nav) {
    background: transparent;
  }
  .img-box{
    width: 45px;
    height: 45px;
  }
  .content {
    background: linear-gradient(145deg, #87CEEB 0%, #87CEFA 100%);
    margin: 0 auto;
    clip-path: ellipse(80% 60% at 50% 40%);
    padding: 200px 0 150px 0;

    > h1 {
      text-align: center;
      font-size: 34px;
      line-height: 52px;
      color: $h1_color;
    }
    >h2 {
      text-align: center;
      //padding-right: 100px;
      font-size: 20px;
      line-height: 26px;
      color: $h1_color;
      margin: 10px 0;
    }
    .btnv{
      text-align: center;
      overflow: hidden;
      height: 40px;
      line-height: 40px;
      .git{
        margin-right: 15px;
      }
      >a {
        background: $bg;
        padding: 8px 20px;
        color: $btn_color;
        border-radius: $border_radius;
      }
    }
  }
  .desc{
    display: flex;
    padding-top: 70px;
    .item{
      flex: 1;
      display: flex;
      justify-content: center;
      >svg{
        width: 45px;
        height: 45px;
        margin-right: 15px;
      }
      .title{
        font-size: 28px;
        margin-bottom: 12px;
      }
      .d-x{
        font-size: 20px;
      }
    }
  }
}
@media screen and (max-width: 900px){
  .home{
    .content{
      padding: 100px 0 50px 0;
      >h2{
        padding-right: 0;
        text-align: center;
        margin-bottom: 15px;
      }
      .btn{
        display: block;
        text-align: center;
        margin: 0 auto;
        width: 300px;
        padding: 0 40px 30px;
        .git{
          margin-right: 0;
          margin-bottom: 15px;
        }
        >a{
          display: inline-block;
          min-width: 8em;
        }
      }
    }
    .desc{
      padding-bottom: 200px;
      flex-direction: column;
      .item{
        display: block;
        text-align: center;
        margin: 0 auto;
        width: 300px;
        padding: 0 40px 30px;
        .title{
          font-size: 20px;
        }
        .d-x{
          font-size: 14px;
          line-height: 20px;
        }
        >svg{
          margin-bottom: 10px;
          margin-right: 0;
        }
      }
    }
  }
}
</style>
