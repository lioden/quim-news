<template>
  <div>
    <br />
    <p class="customtitle text-xs-center">
      Notícias Recentes
    </p>
    <br />
    <hr color="grey" />
    <gridrecentes></gridrecentes>
  </div>
</template>

<script>
import gridrecentes from '~/components/gridrecentes'
export default {
  components: {
    gridrecentes
  }
}
</script>

<style>
p {
  text-shadow: 0px 0px 0px black;
}

.cartao {
  padding-top: 30px;
}
.customtitle {
  font-family: 'Teko', sans-serif;
  font-size: 40px;
}
</style>
