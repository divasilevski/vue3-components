<template lang="pug">
img(alt="Vue logo" src="./assets/logo.png")
.cards
  SimpleCard(
    image="http://orl.ec/images/%D0%9A%D0%BE%D1%82%D0%B8%D0%BA.jpg"
    title="Some title"
    copy="Some copy"
  )
  SimpleCard(
    title="Some title Some subtitle Some subtitle"
    copy="Some copy"
  )
  SimpleCard(
    image="http://orl.ec/images/%D0%9A%D0%BE%D1%82%D0%B8%D0%BA.jpg"
    copy="Some text Some subtitle Some subtitle Some subtitle Some subtitle Some subtitle"
  )

</template>

<script>
import SimpleCard from './components/Cards/SimpleCard.vue'

export default {
  name: 'App',
  components: {
    SimpleCard,
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.cards {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr;
  grid-column-gap: 30px;
  padding: 50px;
}
</style>
