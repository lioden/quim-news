<template>
  <v-carousel hide-delimiters>
    <v-carousel-item v-for="(item, i) in fontes" :key="i" :src="item">
      <div class="overlay"></div>
      <div class="centrado headline">
        <p>{{ titulos[i] }}</p>
      </div>
    </v-carousel-item>
  </v-carousel>
</template>

<script>
export default {
  props: {
    fontes: Array,
    titulos: Array
  }
}
</script>

<style>
.centrado {
  position: absolute;
  left: 10%;
  right: 10%;
  top: 50%;
  color: #fff;
  text-align: center;
  display: inline-block;
  margin: 0 auto;
  z-index: 3;
}

.overlay {
  position: absolute; /* Sit on top of the page content */
  width: 100%; /* Full width (cover the whole page) */
  height: 100%; /* Full height (cover the whole page) */
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background-color: rgba(0, 0, 0, 0.3); /* Black background with opacity */
  z-index: 2; /* Specify a stack order in case you're using a different order for other elements */
}
</style>
