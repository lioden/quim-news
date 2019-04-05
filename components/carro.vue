<template>
  <div>
    <v-carousel hide-delimiters>
      <v-carousel-item v-for="(item, i) in sources" :key="i" :src="item">
        <nuxt-link :to="`/articles/${identificadores[i]}`">
          <div class="overlay"></div>
          <div class="centrado">
            <p>Id da notícia: {{ identificadores[i] }}</p>
          </div>
        </nuxt-link>
      </v-carousel-item>
    </v-carousel>
  </div>
</template>

<script>
export default {
  props: {
    sources: Array,
    identificadores: Array
  },
  data() {
    return {
      items: [
        {
          text: 'Um coelho francês enferniza as populações de Codal',
          src:
            'https://images.unsplash.com/photo-1553634208-34a05bcf43c1?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2000&q=80'
        },
        {
          text: 'Um banco numa cidade qualquer é acessível de metro',
          src:
            'https://images.unsplash.com/photo-1553499972-ef3ae1b36364?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'
        },
        {
          text:
            'Zara de Madaíl declara falência após abertura de loja da Guida',
          src:
            'https://images.unsplash.com/photo-1553499971-87f7a7e1b20a?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1936&q=80'
        },
        {
          text:
            'Está comprovado num estudo realizado por alguém que escrever com um lápis numa folha de papel pode ser considerado estudar',
          src:
            'https://images.unsplash.com/photo-1553419096-efeafe17bbb7?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80'
        }
      ]
    }
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
