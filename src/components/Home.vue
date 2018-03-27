<template>
  <div>
    <img src="../assets/logo.jpeg" class="logo">
    <div class="hello">
    {{ msg }}
    </div>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: '瓜瓜和豆豆,嘻嘻'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .hello{
    font-size: 24px;
    margin: 50px auto;
    color: #6366BD;
  }
  .logo{
    width: 200px;
    height: 260px;
    margin-top: 30px;
    border-radius: 6px;
  }
</style>
