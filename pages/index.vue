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
    <hr class="grey--text" />
    <gridrecentes></gridrecentes>
    <br /><br /><br />
    <hr class="grey--text" />
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
.cartao {
  padding-top: 30px;
}
</style>
