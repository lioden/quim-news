<template>
  <v-card color="grey lighten--1" dark style="box-shadow: 2px 2px 8px 5px grey">
    <v-card color="grey darken-3" dark height="70">
      <v-card-text class="display-1 grey--text text--lighten-3 text-xs-right">
        Latest News
      </v-card-text>
    </v-card>
    <v-layout row wrap>
      <cardlandscape
        v-for="(value, i) in relatedimages"
        :key="i"
        :image="relatedimages[i]"
        :title="relatedtitles[i]"
      ></cardlandscape>
    </v-layout>
  </v-card>
</template>

<script>
import cardlandscape from '~/components/card-landscape'
export default {
  components: {
    cardlandscape
  },
  props: {
    sectiontitle: String,
    relatedimages: Array,
    relatedtitles: Array
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
