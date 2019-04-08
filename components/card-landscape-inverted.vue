<template>
  <v-container fluid grid-list style="padding:10px 5px 0px">
    <v-layout row wrap>
      <v-flex d-flex xs12 md12>
        <v-card color="white darken-2" dark>
          <v-layout row wrap style="margin:0px">
            <v-flex d-flex xs12 md7 class="whitecard">
              <v-container bg fill-height grid-list text-xs-center>
                <v-layout row wrap align-center>
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
.whitecard {
  height: 150px;
  padding: 0px;
  color: black;
  border-style: solid;
  border-width: 0.1px;
  border-color: black;
}
</style>
