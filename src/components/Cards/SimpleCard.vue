<template lang="pug">
.card
  .card__header
    img(:src="image")

  .card__body
    h2.card__title(v-if="title") {{ title }}
    .card__copy(v-if="copy") {{ copy }}
</template>

<script>
export default {
  props: {
    image: {
      type: String,
      default:
        'https://breakthrough.org/wp-content/uploads/2018/10/default-placeholder-image.png',
    },
    title: {
      type: String,
      default: '',
    },
    copy: {
      type: String,
      default: '',
    },
  },
}
</script>

<style lang="scss" scoped>
// variables
$bg: #eeeeee;
$br: 4px;

// classes
.card {
  position: relative;
  background: $bg;
  width: 100%;
  border-radius: $br;

  .card__header {
    height: 300px;

    img {
      width: 100%;
      height: 100%;
      background-size: cover;
      border-top-left-radius: $br;
      border-top-right-radius: $br;
    }
  }

  .card__body {
    padding: 20px;

    .card__title {
      text-align: left;
      margin: 0 0 15px 0;
      font-weight: bold;
      font-size: 20px;
    }

    .card__copy {
      text-align: left;
      margin: 0;
      font-size: 14px;
    }
  }
}
</style>
