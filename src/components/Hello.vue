<template>
  <div class="hello">
    <!-- 图片 -->
    <img class="details-img" src="../assets/bitmap.jpg">

    <!-- 内容 -->
    <div class="details-content">
      <!-- 标题 -->
      <h3>{{detailsTitle}}</h3>
      <!-- 简介 -->
      <div class="details-brief">
        <div class="brief-head-portrait">
          <img class="details-img" src="../assets/bitmap.jpg">
        </div>
        <h4 class="brief-name">{{briefName}}</h4>
        <p class="brief-text">{{briefText}}</p>
      </div>

      <!-- 功效原理 -->
      <div class="details-effect">
        <h4 class="effect-title">
          {{effectTitle}}
        </h4>
        <p class="effect-text">
          {{effectText}}
        </p>
      </div>

      <!-- 准备 -->
      <div class="details-ready">
        <h4 class="effect-title ready-title">
          {{detailsTitle}}
        </h4>
        <get-ready-list>
        </get-ready-list>
      </div>
    </div>
  </div>
</template>

<script>
import getReadyList from './modular/get-ready-list'
export default {
  name: 'hello',
  data () {
    return {
      detailsTitle: '方法名称',
      briefName: '无忌老师',
      briefText: '一款滋阴，生津，补气，养血的美颜汤 ，特别适合冬季感觉干燥，有虚火的你。养生从补肾开始 ，补肾从九蒸九晒的芝麻丸开始，有虚火的你。',
      effectTitle: '功效原理',
      effectText: '山楂十几颗或炒山楂肉，冰糖适量,松树四季常青，不论平原还是高山，松树都能扎根生长，生命力十分顽强。孔子云「岁寒，然后知松柏之后凋也。」',
      detailsTitle: '准备',
      msg: 'Welcome to Your Vue.js App'
    }
  },
  created:function(){
    this.$http.post('***',
                { }).then((response) => {
        this.articles = response.data.data.list;
      }).catch(function(response) {
        console.log(response)
      });

  },
  components:{
    getReadyList
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
.details-img{
  width:100%;
  height:2.4rem;
}
.details-content{
  padding:0.3rem .15rem 0;
}
.details-content > h3{
  font-size:.18rem;
  color:#333;
  line-height:.23rem;
  padding-bottom:.51rem;
  font-weight: 600;
}
.details-brief{
  position: relative;
  padding-top:.33rem;
  margin-left:.35rem;
  width:2.75rem;
  border:1px solid #afafaf;
  border-radius:5px;
}
.brief-head-portrait{
  width:.44rem;
  height:.44rem;
  background:#d8d8d8;
  border-radius:50%;
  position: absolute;
  top:0;
  left: 50%;
  margin-left: -0.22rem;
  margin-top: -0.22rem;
  z-index: 1;
  overflow: hidden;
}
.brief-head-portrait > img{
  width:100%;
  height:100%;
}
.brief-name{
  font-size:.16rem;
  color:#333;
  line-height:.18rem;
  font-weight:500;
}
.brief-text{
  display: inline-block;
  width:100%;
  margin-top:.05rem;
  padding:0 .15rem;
  font-size:.13rem;
  color:#555;
  font-weight:500;
}
.details-effect{
  margin-top:.41rem;
}
.effect-title{
  padding:0.01rem 0;
  font-size:.16rem;
  color:#333;
  text-align:left;
  line-height:.18rem;
  font-weight:500;
  background:url(../assets/icon01.png) no-repeat;
  background-size: .2rem;
  background-position: 0 -0.01rem;
  text-indent: .3rem;
}
.effect-text{
  margin-top:.2rem;
  font-size:.14rem;
  line-height:.28rem;
  color:#555;
  text-align:left;
  padding-bottom:.2rem;
  border-bottom:.02rem solid #afafaf;
}
.details-ready{
  margin-top:.4rem;
}
.ready-title{
  margin-bottom:.05rem;
}
</style>
