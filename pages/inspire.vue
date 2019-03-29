<template>
  <div>
    <v-container fluid grid-list-lg>
      <v-layout row wrap>
        <v-flex d-flex xs8>
          <v-layout row wrap>
            <v-flex d-flex xs8>
              <v-card color="indigo lighten-2" dark tile flat>
                card1
              </v-card>
            </v-flex>
            <v-flex d-flex xs4>
              <v-card color="indigo lighten-2" dark tile flat>
                card2
              </v-card>
            </v-flex>
            <v-flex d-flex xs4>
              <v-card color="yellow lighten-2" dark tile flat>
                card3
              </v-card>
            </v-flex>
            <v-flex d-flex xs8>
              <v-card color="yellow lighten-2" dark tile flat>
                card4
              </v-card>
            </v-flex>
            <v-flex d-flex xs12>
              <v-card color="black lighten-2" dark tile flat>
                card5
              </v-card>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs4>
          <v-card color="red lighten-2" dark tile flat>
            Latest News
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <div>
      <cardsone />
      <cardsone />
    </div>
    <div>
      <cardsone />
    </div>
  </div>
</template>

<script>
import cardsone from '~/components/cardsection-one'
export default {
  components: {
    cardsone
  },
  data: () => ({
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`
  })
}
</script>
