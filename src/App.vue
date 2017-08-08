<template>
  <div id="app">
    <div class="wrap">
      <index-list :data="playerList" v-if="playerList.length"></index-list>
    </div>
  </div>
</template>

<script>
import IndexList from './components/index-list'

export default {
  name: 'app',
  data() {
    return {
      playerList: [/*test data in testData.json*/]
    }
  },
  components: {
    IndexList
  }
}
</script>

<style lang="stylus">
  *
    margin:0
    padding:0
</style>

