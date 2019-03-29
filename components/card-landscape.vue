<template>
  <v-container fluid grid-list-xl>
    <v-layout row wrap>
      <v-flex d-flex xs12 md12>
        <v-card color="red lighten-1" dark>
          <v-layout row wrap>
            <v-flex d-flex xs12 md4>
              <v-card color="red lighten-2" dark>
                <v-img
                  src="https://media.wired.com/photos/5c9d205d1e34481170ef2c00/1:1/w_326,c_limit/Culture_Replay_Ninja-1054424402.jpg"
                ></v-img>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md8>
              <v-card color="grey darken-3" dark>
                <v-card-title primary class="title">Lorem</v-card-title>
                <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    one:
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
  })
}
</script>
