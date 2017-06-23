<template>

  <router-link to='../' name="get-ready-list" class="clearfix get-ready-list">
  	<div class="get-ready-img" v-bind:style="{backgroundImage: 'url(' + albumpic_big + ')'}"></div>
	<div class="get-ready-content">
	  <h3>{{getContentTitle}}</h3>
	  <div class="getTeadyCenter clearfix">
	  	<get-lable v-bind:getLable="lable" v-for='lable in onLable'></get-lable>
	  </div>
  	</div>
  </router-link>
</template>
<script>
  import getLable from './get-lable'
  export default {
  	name: 'get-ready-list',
  	data(){
  	  return{
		albumpic_big: '/static/img/bitmap.d0c62a1.jpg',
  	    getContentTitle: '商品标题纯藕粉，热水冲调',
  	    onLable:[
  	      {content:"体质"},
  	      {content:"慢性病"},
  	      {content:"体质"},
  	      {content:"慢性病"},
  	      {content:"症状"}
  	    ]
  	  }
  	},
  	components:{
  		getLable
  	}
  }
</script>

<style>
.get-ready-list{
	display:block;
	padding:.15rem 0;
	border-bottom:1px solid #afafaf;
}
.get-ready-img{
	float:left;
	width:1.06rem;
	height:.8rem;
	background-size: cover;
	background-position: center center;
}
.get-ready-content{
	float:left;
	width:2.39rem;
	padding-left:.15rem;
}
.get-ready-content > h3{
	font-size:.15rem;
	color:#333;
	text-align:left;
	line-height:.18rem;
	font-weight:500;
	overflow: hidden;
	text-overflow:ellipsis;
	white-space: nowrap;
}
.getTeadyCenter{
	width:100%;
	height:.18rem;
	overflow: hidden;
	margin-top:.1rem;
	margin-bottom:.1rem;
}
</style>
