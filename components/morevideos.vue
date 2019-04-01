<template>
  <v-layout row wrap>
    <v-flex d-flex>
      <v-layout row wrap>
        <v-flex d-flex xs12>
          <v-card
            color="grey darken-2"
            dark
            style="box-shadow: 2px 2px 8px 5px grey"
          >
            <v-card color="blue darken-3" dark height="70">
              <v-card-text
                class="headline white--text text--lighten-3 text-xs-left"
              >
                Related Videos
              </v-card-text>
            </v-card>
            <br />
            <videothumb></videothumb>
            <videothumb></videothumb>
            <videothumb></videothumb>
            <videothumb></videothumb>
            <videothumb></videothumb>
          </v-card>
        </v-flex>
      </v-layout>
    </v-flex>
  </v-layout>
</template>

<script>
import videothumb from '~/components/videothumb'
export default {
  components: {
    videothumb
  },
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    one:
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
  })
}
</script>
