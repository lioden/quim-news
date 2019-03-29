<template>
  <div>
    <tabsverticais />
    <v-container fluid grid-list-md>
      <v-layout row wrap>
        <v-flex d-flex xs12 sm6 md3>
          <carro />
        </v-flex>
        <v-flex d-flex xs12 sm6 md3>
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12>
                  <carro />
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 sm6 md3>
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12>
                  <carro />
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 sm6 md3>
          <v-layout row wrap>
            <v-flex d-flex>
              <v-layout row wrap>
                <v-flex d-flex xs12>
                  <carro />
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
      </v-layout>
    </v-container>
    <v-container fluid grid-list-md>
      <v-layout row wrap>
        <v-flex d-flex xs12 sm6 md6>
          <carro />
        </v-flex>
        <v-flex d-flex xs12 sm6 md6>
          <carro />
        </v-flex>
      </v-layout>
    </v-container>
    <p class="font-weight-bold display-1" style="padding-left:10px">
      <bold>Notícias Recentes</bold>
    </p>
    <hr />
    <tabsverticais style="padding-top:20px" />
    <row4cards />
    <minicards />
  </div>
</template>

<script>
import tabsverticais from '~/components/tabsverticais'
import carro from '~/components/carro'
import minicards from '~/components/minicards'
import row4cards from '~/components/row4cards'
export default {
  components: {
    tabsverticais,
    carro,
    row4cards,
    minicards
  },
  data: () => ({
    show: false
  })
}
</script>

<style>
.cartao {
  padding-top: 30px;
}
</style>
