<template>
  <div class="sh-view">
    <div class="sh-key">{{keyword}}</div>
  </div>
</template>

<script>
export default {
  name: 'searchhead',
  data () {
    return {
      keyword: this.$route.params.keyword
    }
  },
  watch: {
    '$route' (to, from) {
      if (to.name === 'search') {
        this.keyword = this.$route.params.keyword
      }
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.sh-view{
  padding: 0 20px;
}
.sh-key{
  float: left;
}
</style>
