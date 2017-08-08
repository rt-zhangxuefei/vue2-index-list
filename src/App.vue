<template>
  <div id="app">
    <div class="wrap">
      <index-list :data="playerList" @choose="onChoose" v-if="playerList.length"></index-list>
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
  methods: {
    onChoose(item) {
      console.log(item)
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

