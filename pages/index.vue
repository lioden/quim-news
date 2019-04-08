<template>
  <div>
    <br />
    <p
      class="font-weight-regular display-1 blue--text text--darken-2 text-xs-right"
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
  text-shadow: 0px 0px 0px black;
}

.cartao {
  padding-top: 30px;
}
</style>
