<template>
  <div>
    <br />
    <p
      class="font-weight-bold display-1 grey--text text--lighten-3 text-xs-right"
      style="padding-left:10px"
    >
      Notícias Recentes
    </p>
    <hr class="grey--text" />
    <grid></grid>
    <br /><br /><br />
    <p
      class="font-weight-bold display-1 black--text text--lighten-3 text-xs-left"
      style="padding-left:10px"
    >
      Ver Mais
    </p>
    <hr class="grey--text" />
    <row4cards />
  </div>
</template>

<script>
import row4cards from '~/components/row4cards'
import grid from '~/components/grid'
export default {
  components: {
    row4cards,
    grid
  }
}
</script>

<style>
.cartao {
  padding-top: 30px;
}
</style>
