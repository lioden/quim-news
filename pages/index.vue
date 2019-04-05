<template>
  <div>
    <br />
    <p
      class="font-weight-bold display-1 grey--text text--lighten-3 text-xs-right"
      style="padding-left:10px"
    >
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
  font-weight: bold;
  text-shadow: 0px 1px 2px black;
}

.cartao {
  padding-top: 30px;
}
</style>
