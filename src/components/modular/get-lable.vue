<template>
  <div name="lable" class="lable">
  	{{getLable.content}}
  </div>
</template>
<script>
  export default {
  	props:["getLable"]
  }	
</script>
<style>
.lable{
	float:left;
	display:inline-block;
	font-size:.12rem;
	margin-bottom:2rem;
	text-align:left;
	color:#299939;
	padding:0 .1rem;
	border:1px solid #299939;
	border-radius:5px;
	line-height:1.4;
	margin-right:.1rem;
}
</style>