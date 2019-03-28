<template>
  <v-container fluid grid-list-md>
    <v-layout row wrap>
      <v-flex d-flex xs12 sm6 md3>
        <v-card color="purple" dark>
          <v-img :src="one"></v-img>
          <v-card-title primary class="title">Lorem</v-card-title>
          <v-card-text>{{ lorem }}</v-card-text>
        </v-card>
      </v-flex>
      <v-flex d-flex xs12 sm6 md3>
        <v-layout row wrap>
          <v-flex d-flex>
            <v-card color="red lighten-2" dark>
              <v-img
                src="https://images.unsplash.com/photo-1553671972-15e7bef005d7?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&h=630&q=80"
              ></v-img>
              <v-card-title primary class="title">Lorem</v-card-title>
              <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex d-flex xs12 sm6 md3>
        <v-layout row wrap>
          <v-flex d-flex>
            <v-card color="green lighten-2" dark>
              <v-img
                src="https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&h=630&q=80"
              ></v-img>
              <v-card-title primary class="title">Lorem</v-card-title>
              <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex d-flex xs12 sm6 md3>
        <v-layout row wrap>
          <v-flex d-flex>
            <v-card color="blue lighten-2" dark>
              <v-img
                src="https://images.unsplash.com/photo-1553434446-6259e914ddc3?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&h=630q=80"
              ></v-img>
              <v-card-title primary class="title">Lorem</v-card-title>
              <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
            </v-card>
          </v-flex>
        </v-layout>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    one:
      'https://images.unsplash.com/photo-1553310871-5f7d4a4eb6b8?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&h=630&q=80'
  })
}
</script>
