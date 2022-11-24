<template>
  <main>
    <div id="app">
      <nft-card :heading="heading" :body="body" :author="author" :price="price" :time="time" />
    </div>
  </main>
</template>

<script>
import NftCard from './components/nft-card.vue'

export default {
  name: 'App',
  components: {
    NftCard
  },
  data: function() {
    return {
      heading: 'Equilibrium #3429',
      body: 'Our Equilibrium collection promotes balance and calm.',
      author: 'Jules Wyvern',
      price: '0.041',
      time: '3'
    }
  }
}
</script>

<style>
#app {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
</style>
