<template>
  <v-container fluid grid-list-md>
    <v-layout row wrap>
      <v-flex d-flex xs12 sm6 md5 style="padding-right:1.5%">
        <v-card color="grey darken-3" dark height="800">
          <v-img :src="one" style="min-height:400px;max-height:500px"></v-img>
          <v-card-title primary class="title">Lorem</v-card-title>
          <v-card-text>{{ lorem }}</v-card-text>
        </v-card>
      </v-flex>
      <v-flex d-flex xs12 sm6 md3>
        <v-layout row wrap>
          <v-flex d-flex>
            <v-layout row wrap>
              <v-flex v-for="n in 1" :key="n" d-flex xs12>
                <v-card color="red lighten-2" dark height="800">
                  <v-img
                    style="min-height:400px;max-height:500px"
                    src="https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
                  ></v-img>
                  <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
                </v-card>
              </v-flex>
            </v-layout>
          </v-flex>
        </v-layout>
      </v-flex>
      <v-flex d-flex xs12 sm6 md4 style="padding-left:1.5%;">
        <v-layout row wrap>
          <v-flex d-flex style="box-shadow: 2px 2px 8px 5px grey;">
            <v-layout row wrap>
              <v-flex v-for="n in 1" :key="n" d-flex xs12>
                <v-card color="grey lighten-2" dark>
                  <v-card color="grey darken-2" dark height="70">
                    <v-card-text
                      class="display-1 grey--text text--lighten-3 text-xs-right"
                    >
                      Latest News
                    </v-card-text>
                  </v-card>
                  <br />
                  <v-card
                    color="grey lighten-3"
                    dark
                    height="200"
                    style="padding-top:10px"
                  >
                    <v-card-text class="body-1 grey--text text--darken-3">{{
                      lorem
                    }}</v-card-text>
                  </v-card>
                  <br />
                  <v-card
                    color="grey lighten-3"
                    dark
                    height="200"
                    style="padding-top:10px"
                  >
                    <v-card-text class="body-1 grey--text text--darken-3">{{
                      lorem
                    }}</v-card-text>
                  </v-card>
                  <br />
                  <v-card
                    color="grey lighten-3"
                    dark
                    height="200"
                    style="padding-top:10px"
                  >
                    <v-card-text class="body-1 grey--text text--darken-3">{{
                      lorem
                    }}</v-card-text>
                  </v-card>
                  <br />
                  <v-card
                    color="grey lighten-3"
                    dark
                    height="200"
                    style="padding-top:10px"
                  >
                    <v-card-text class="body-1 grey--text text--darken-3">{{
                      lorem
                    }}</v-card-text>
                  </v-card>
                </v-card>
              </v-flex>
            </v-layout>
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
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
  })
}
</script>
