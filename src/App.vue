<template>
  <div id="app">
    <header>
      <span>{{tleHtml}}</span>
      <searchhead v-if="!tleHtml" />
    </header>
    <router-view/>
    <ul class="footer">
      <li class="home">
        <router-link to="/"></router-link>
      </li>
      <li class="order">
        <router-link to="/order"></router-link>
      </li>
      <li class="history"></li>
      <li class="my"></li>
    </ul>
  </div>
</template>

<script>
import SearchHead from './components/SearchHeader'
export default {
  name: 'App',
  data () {
    return {
      tleHtml: '首页'
    }
  },
  components: {
    searchhead: SearchHead
  },
  watch: {
    '$route' (to, from) {
      switch (to.name) {
        case 'home':
          this.tleHtml = '首页'
          break
        case 'order':
          this.tleHtml = '音图表'
          break
        case 'search':
          this.tleHtml = ''
          break
      }
    }
  }
}
</script>

<style>
html,body,div,span,applet,object,iframe,h1,h2,h3,h4,h5,h6,p,blockquote,a,abbr,acronym,address,big,cite,code,del,dfn,em,font,img,ins,kbd,q,s,samp,small,strike,strong,sub,sup,tt,var,dl,dt,dd,ol,ul,li,fieldset,form,label,legend,table,caption,tbody,tfoot,thead,tr,th,td{
  margin:0;
  padding:0;
  border:0;
  outline:0;
  font-weight:inherit;
  font-style:inherit;
  font-size:100%;
  font-family:inherit;
  vertical-align:baseline;
}
html{
  font-size:101%;
  font-family:Arial,verdana,arial,sans-serif;
  font-size:12px;
  -webkit-text-size-adjust:none;
  color:#6F6F6F;
}
body{
  min-height:100%;
  height:auto;
  width:100%;
}
header{
  position: fixed;
  height: 60px;
  width: 100%;
  background: #6366BD;
  margin-top: -60px;
  text-align: center;
  line-height: 60px;
  color: white;
  font-size: 24px;
}
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  background: white;
}

.footer{
  position: fixed;
  bottom:0;
  list-style-type: none;
  padding: 0;
  margin:0;
  width: 100%;
  padding: 10px 0;
  border-top: 3px solid #efefef;
}
.footer li {
  display: inline-block;
  margin: 0px;
  width: 24%;
  height: 45px;
  background-position: center;
}
.home{
  background: url(./assets/11.png) no-repeat;
}
.order{
  background: url(./assets/21.png) no-repeat;
}
.history{
  background: url(./assets/31.png) no-repeat;
}
.my{
  background: url(./assets/41.png) no-repeat;
}
.footer li a{
  display: block;
  width: 100%;
  height: 100%;
}
</style>
