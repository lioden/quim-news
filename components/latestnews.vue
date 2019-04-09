<template>
  <v-layout row wrap>
    <v-flex d-flex>
      <v-layout row wrap>
        <v-flex d-flex xs12>
          <v-card color="#0277bd" dark style="box-shadow: 1px 1px 2px 2px grey">
            <v-card color="white darken-3" dark>
              <v-card-text
                class="black--text text--darken-1 text-xs-right customtitle"
              >
                Últimas Notícias
              </v-card-text>
            </v-card>
            <hr />
            <cardlandscape
              v-for="(value, i) in images.slice(0, 4)"
              :key="i"
              class="hoverable"
              :image="images[i]"
              :title="titles[i]"
            ></cardlandscape>
            <cardlandscapeinv
              v-for="(value, i) in images.slice(4, 9)"
              :key="(i = i + 4)"
              class="hoverable"
              :image="images[i]"
              :title="titles[i]"
            ></cardlandscapeinv>
            <br />
          </v-card>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
import cardlandscape from '~/components/card-landscape'
import cardlandscapeinv from '~/components/card-landscape-inverted'
export default {
  components: {
    cardlandscape,
    cardlandscapeinv
  },
  props: {
    images: Array,
    titles: Array
  },
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    one:
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
  })
}
</script>

<style>
.gradient {
  background-image: linear-gradient(
    180deg,
    black -25%,
    RoyalBlue 35%,
    RoyalBlue 65%,
    black 125%
  );
}
</style>
