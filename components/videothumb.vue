<template>
  <v-container>
    <v-layout row wrap>
      <v-flex d-flex xs12 md12>
        <v-card color="blue lighten-1" dark>
          <v-layout row wrap>
            <v-flex d-flex xs12 md5>
              <v-card color="grey darken-3" dark>
                <v-img
                  src="https://images.unsplash.com/photo-1553800391-d3c38ac58ab2?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=2145&q=80"
                  style="height:130px"
                ></v-img>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md7>
              <v-card color="grey lighten-3" dark>
                <v-card-title primary class="title black--text"
                  >Video Title</v-card-title
                >
                <v-card-text class="black--text">
                  Video description
                </v-card-text>
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
