<template>
  <v-container fluid grid-list style="padding:0px 10px 15px">
    <v-container fluid grid-list style="padding:0px 10px 15px">
      <v-layout row wrap>
        <v-flex d-flex xs6 md12>
          <v-card color="grey darken-3" dark>
            <v-layout row wrap style="margin:0px">
              <v-flex d-flex xs12 md5 style="padding:0px">
                <v-img
                  style="object-fit: fill; height:150px"
                  src="https://images.unsplash.com/photo-1509085443839-d64c1b6eb61b?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=1350&q=80"
                ></v-img>
              </v-flex>
              <v-flex d-flex xs12 md7 style="height:150px;padding:0px">
                <v-container
                  bg
                  fill-height
                  grid-list
                  text-xs-center
                  style="padding:0px"
                >
                  <v-layout row wrap align-center style="padding:0px">
                    <v-flex class="hifens">
                      <p>Coelho francês inferniza as populações de Codal</p>
                    </v-flex>
                  </v-layout>
                </v-container>
              </v-flex>
            </v-layout>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
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
