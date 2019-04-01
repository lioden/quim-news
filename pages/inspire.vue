<template>
  <div>
    <!-- Primeira Grid -->
    <v-container fluid grid-list-xl>
      <v-layout row wrap>
        <v-flex d-flex xs12 md8>
          <v-layout row wrap>
            <v-flex d-flex xs12 md8>
              <v-card color="red lighten-2" dark>
                <!-- o array funciona, {{ arraycarro1.images[0] }} passar para o componente -->
                <carro></carro>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md4>
              <v-card color="grey darken-3" dark>
                <carro></carro>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md6>
              <v-layout row wrap>
                <v-flex d-flex xs6 md12>
                  <cardlandscape></cardlandscape>
                </v-flex>
                <v-flex d-flex xs6 md12>
                  <cardlandscape></cardlandscape>
                </v-flex>
              </v-layout>
            </v-flex>
            <v-flex d-flex xs12 md6>
              <v-card color="green darken-3" dark height="400">
                <iframe
                  width="100%"
                  height="100%"
                  src="https://www.youtube.com/embed/R_uS0aT0bG8"
                  frameborder="0"
                  allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                  allowfullscreen
                ></iframe>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md12>
              <v-card color="black lighten-2" dark height="400">
                <v-img
                  style="min-height:250px;max-height:250px"
                  src="https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80"
                ></v-img>
                <v-card-text>{{ lorem.slice(0, 40) }}</v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 md4>
          <latestnews></latestnews>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Fim da primeira grid -->
    <br />
    <hr />
    <br />
    <!-- Segunda grid -->
    <v-container fluid grid-list-xl>
      <v-layout row wrap>
        <v-flex d-flex xs12 md9>
          <v-layout row wrap>
            <v-flex d-flex xs12 md12>
              <iframe
                width="100%"
                height="700px"
                src="https://www.youtube.com/embed/JYjIlHWBAVo"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </v-flex>
            <v-flex d-flex xs12 md12>
              <v-layout row wrap>
                <v-flex d-flex xs6 md12>
                  <v-card color="grey lighten-3" dark>
                    <v-card-title primary class="title black--text"
                      >Infected Mushroom - Guitarmass</v-card-title
                    >
                    <v-card-text class="black--text caption text-xs-right">
                      01/04/2019
                    </v-card-text>
                    <v-card-text class="black--text">
                      Stream/Download: ➥ https://monstercat.ffm.to/guitarmass 🎧
                      Genre: #Psytrance
                    </v-card-text>
                    <v-card-text class="black--text caption">
                      Infected Mushroom
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 md3>
          <morevideos></morevideos>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Fim da segunda grid -->
    <br />
    <hr />
    <br />
  </div>
</template>

<script>
import latestnews from '~/components/latestnews'
import morevideos from '~/components/morevideos'
import cardlandscape from '~/components/card-landscape'
import carro from '~/components/carro'
export default {
  components: {
    latestnews,
    cardlandscape,
    carro,
    morevideos
  },
  data: () => ({
    arraycarro1: {
      images: [
        'https://images.unsplash.com/photo-1553722686-e94d1b20e9e0?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80',
        'https://images.unsplash.com/photo-1553808744-634be53ea568?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=700&q=80'
      ],
      texts: [
        'Uma caixa de correio random no meio duma ponte',
        'A filha da Maria comprou um chapéu novo'
      ]
    },
    lorem: `Lorem ipsum dolor sit amet, mel at clita quando. Te sit oratio vituperatoribus, nam ad ipsum posidonium mediocritatem, explicari dissentiunt cu mea. Repudiare disputationi vim in, mollis iriure nec cu, alienum argumentum ius ad. Pri eu justo aeque torquatos.`,
    one:
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80'
  })
}
</script>
