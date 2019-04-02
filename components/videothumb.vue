<template>
  <v-container>
    <v-layout row wrap>
      <v-flex d-flex xs12 md12>
        <v-card color="grey darken-2" dark>
          <v-layout row wrap>
            <v-flex d-flex xs12 md5>
              <v-card color="black darken-3" dark>
                <v-img
                  style="object-fit: fill; height:160px"
                  src="https://images.unsplash.com/photo-1554186285-e2bc44c34216?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
                ></v-img>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md7>
              <v-container bg fill-height grid-list-md text-xs-center>
                <v-layout row wrap align-center>
                  <v-flex>
                    Agressões no Hóquei
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
