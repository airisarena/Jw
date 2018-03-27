<template>
  <div class="order-view">
    <ul class="order-table">
      <li v-for="i in list" v-bind:key="i">
        <router-link :to="{name: 'search',  params: {keyword : i}}">{{i}}</router-link>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      list: ['あ', 'い', 'う', 'え', 'お', 'か', 'き', 'く', 'け', 'こ',
        'さ', 'し', 'す', 'せ', 'そ', 'た', 'ち', 'つ', 'て', 'と',
        'な', 'に', 'ぬ', 'ね', 'の', 'は', 'ひ', 'ふ', 'へ', 'ほ',
        'ま', 'み', 'む', 'め', 'も', 'ら', 'り', 'る', 'れ', 'ろ',
        'や', 'ゆ', 'よ', 'わ', 'を'
      ]
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
  .order-view{
    padding-top: 30px;
  }
  .order-table{
    width: 90%;
    margin: 20px auto;
    font-size: 20px;
    font-weight: bold;
  }
  .order-table li{
    display: inline-block;
    width: 19%;
    height: 45px;
    line-height: 45px;
    border: 1px solid #6366BD;
  }
  .order-table li a{
    text-decoration: none;
    color: #555;
  }
</style>
