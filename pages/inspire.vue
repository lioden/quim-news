<template>
  <div>
    <v-container fluid grid-list-xl>
      <v-layout row wrap>
        <v-flex d-flex xs12 md8>
          <v-layout row wrap>
            <v-flex d-flex xs12 md8>
              <v-card color="red lighten-2" dark>
                <v-img
                  style="min-height:250px;max-height:350px"
                  src="https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
                ></v-img>
                <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md4>
              <v-card color="grey darken-3" dark>
                <carro></carro>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md6>
              <v-layout row wrap>
                <v-flex d-flex xs6 md12>
                  <v-card color="blue lighten-2" dark height="185">
                    some text
                  </v-card>
                </v-flex>
                <v-flex d-flex xs6 md12>
                  <v-card color="blue lighten-2" dark height="185">
                    some text
                  </v-card>
                </v-flex>
              </v-layout>
            </v-flex>
            <v-flex d-flex xs12 md6>
              <v-card color="green darken-3" dark height="400">
                <v-img
                  style="min-height:250px;max-height:250px"
                  src="https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
                ></v-img>
                <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md12>
              <v-card color="black lighten-2" dark height="400">
                <v-img
                  style="min-height:250px;max-height:250px"
                  src="https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
                ></v-img>
                <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 md4>
          <latestnews></latestnews>
        </v-flex>
      </v-layout>
      <cardlandscape></cardlandscape>
    </v-container>
  </div>
</template>

<script>
import latestnews from '~/components/latestnews'
import cardlandscape from '~/components/card-landscape'
import carro from '~/components/carro'
export default {
  components: {
    latestnews,
    cardlandscape,
    carro
  },
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    one:
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
  })
}
</script>
