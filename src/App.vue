<template>
  <div id="app">
    <div class="wrap">
      <index-list :data="playerList" :useLazyLoad="true" @choose="onChoose" v-if="playerList.length"></index-list>
    </div>
  </div>
</template>

<script>
import IndexList from './components/IndexList'
import playerList from './testData.json'

export default {
  name: 'app',
  data() {
    return {
      playerList
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

<style lang="less">
* {
  margin: 0;
  padding: 0;
}
.wrap {
  position: fixed;
  top: 0;
  bottom: 0;
  width: 100%;
}
</style>
