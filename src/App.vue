<template>
  <div id="app">
    <router-view></router-view>
  </div>
</template>

<script>
export default {
  name: 'app'
}
</script>

<style>
* {
    -webkit-box-sizing: border-box;
    -moz-box-sizing: border-box;
    box-sizing: border-box;
}

html,
body {
    min-height: 100%;
    overflow-x: hidden;
}

html {
    -ms-text-size-adjust: 100%;
    -webkit-text-size-adjust: 100%;
    -webkit-tap-highlight-color: rgba(0, 0, 0, 0);
}

a,
img,
body,
button,
div,
fieldset,
form,
h1,
h2,
h3,
h4,
h5,
h6,
html,
img,
input,
li,
menu,
ol,
p,
textarea,
ul,
figure,
dl,
dt,
dd {
    padding: 0;
    margin: 0;
    border: 0;
}

li,
ul,
dl,
dt,
dd {
    list-style: none
}

b,
em,
h1,
h2,
h3,
h4,
h5,
h6,
i,
th,
td {
    font-weight: 400;
    font-style: normal
}

body,
button,
input,
select,
textarea,
img {
    font: 400 0.24rem/1.5 "PingFangSC-Light","DroidSans",-apple-system-font,"Helvetica Neue",Helvetica,Arial,sans-serif;
    outline: 0;
    color: #000;
}

button,
input[type=button],
input[type=password],
input[type=submit],
input[type=text],
textarea {
    -webkit-appearance: none
}

a,
a:visited {
    text-decoration: none;
    color: #5c5658
}

.img img,
video {
    vertical-align: middle
}

img {
    vertical-align: middle;
    border: 0;
    max-width: 100%;
}

body {
    min-width: 320px;
    background: #fff;
    overflow: hidden;
}

.clear:after {
    content: '';
    display: block;
    clear: both
}

#app {
    font-family: 'Avenir', Helvetica, Arial, sans-serif;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
    text-align: center;
    color: #2c3e50;
}
.clearfix:after{
    display:block;
    clear:both;
    content:"";
    visibility:hidden;
    height:0；
} 
.clearfix{
    zoom:1；
} 
</style>
