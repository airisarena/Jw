<template>
  <div class="search-list">
    {{$route.params.keyword}}
  </div>
</template>

<script>
export default {
  name: 'search',
  data () {
    return {}
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.search-list{
  position: fixed;
  top: 60px;
  bottom: 72px;
  width: 100%;
}
</style>
