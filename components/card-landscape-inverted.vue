<template>
  <v-container fluid grid-list style="padding:0px 5px 0px">
    <v-layout row wrap>
      <v-flex d-flex xs12 md12>
        <v-card color="grey darken-3" dark>
          <v-layout row wrap style="margin:0px">
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
                    <p>{{ title }}</p>
                  </v-flex>
                </v-layout>
              </v-container>
            </v-flex>
            <v-flex d-flex xs12 md5 style="padding:0px">
              <v-img
                style="object-fit: fill; height:150px"
                :src="image"
              ></v-img>
            </v-flex>
          </v-layout>
        </v-card>
      </v-flex>
    </v-layout>
  </v-container>
</template>

<script>
export default {
  props: {
    title: String,
    image: String
  },
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    one:
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
  })
}
</script>

<style>
p {
  overflow-x: hidden;
  overflow-y: hidden;
  word-wrap: break-word;
  -webkit-hyphens: auto;
  -moz-hyphens: auto;
  -ms-hyphens: auto;
  hyphens: auto;
}
</style>
