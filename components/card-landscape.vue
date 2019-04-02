<template>
  <v-container fluid grid-list>
    <v-layout row wrap>
      <v-flex d-flex xs12 md12>
        <v-card color="grey darken-3" dark>
          <v-layout row wrap>
            <v-flex d-flex xs12 md5>
              <v-card color="grey darken-3" dark>
                <v-img
                  style="object-fit: fill; height:150px"
                  src="https://images.unsplash.com/photo-1553978370-b05b10c2ddfb?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
                ></v-img>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md7 style="padding-right:10px">
              <v-container bg fill-height grid-list-md text-xs-center>
                <v-layout row wrap align-center>
                  <v-flex>
                    Greve dos estacionamentos em Madaíl
                  </v-flex>
                </v-layout>
              </v-container>
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
