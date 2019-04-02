<template>
  <div>
    <!-- Primeira Grid -->
    <v-container fluid grid-list-s>
      <v-layout row wrap>
        <v-flex d-flex xs12 md9>
          <v-layout row wrap>
            <v-flex d-flex xs12 md12>
              <v-flex d-flex xs12 md12>
                <v-layout row wrap>
                  <v-flex d-flex xs12 md12 style="padding-right:10px;">
                    <v-card color="grey lighten-3" dark>
                      <v-card-text
                        class="black--text display-2 text-xs-center"
                        style="padding-top:30px"
                      >
                        Coelho francês inferniza as populações de Codal
                      </v-card-text>
                      <v-card-text class="black--text caption text-xs-right">
                        01/04/2019
                      </v-card-text>
                    </v-card>
                  </v-flex>
                </v-layout>
              </v-flex>
            </v-flex>
            <v-flex d-flex xs12 md4 style="padding-top:10px">
              <morevideos title="Notícias relacionadas"></morevideos>
            </v-flex>
            <v-flex d-flex xs12 md8>
              <v-layout row wrap>
                <v-flex
                  d-flex
                  xs12
                  md12
                  style="padding-left:10px; padding-right:10px"
                >
                  <v-card color="grey lighten-3" dark>
                    <carroartigo style="height:40%; width:100%"></carroartigo>
                    <br />
                    <hr />
                    <br />
                    <v-card-text class="black--text subheading">
                      <p>
                        Nesta madrugada, dia 1 de Abril de 2019, um dia
                        especialmente conhecido por falsas verdades, foi
                        avistado um coelho francês no vilarejo de Codal por
                        habitantes locais, que se deslocavam ás para as suas
                        habitações após uma longa noite de trabalho na Vicaima.
                      </p>
                      <p>
                        O caos geral instalou-se na localidade, onde se
                        presenciaram momentos extremamente emotivos. As mulheres
                        choravam a partida dos homens para combate, crianças
                        abraçavam as vestes das mães em confusão e homens de
                        família geravam sons femininos e enquanto desviavam
                        investidas ofensivas do inimigo.
                      </p>
                      <p>
                        O presidente da câmara de Vale de Cambra já pediu
                        auxílio ao exército português, mas a recente tragédia da
                        cabrita em Madaíl fragilizou severamente as tropas. Este
                        será um longo dia para os habitantes de Codal, que terão
                        que enfretar a fofura e correrias do Coelho a que
                        denominamos: French Buns.
                      </p>
                    </v-card-text>
                    <v-card-text class="black--text caption text-xs-right">
                      Author: Senhor Joaquim
                    </v-card-text>
                  </v-card>
                </v-flex>
              </v-layout>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 md3>
          <latestnews class="hidden-sm-and-down"></latestnews>
        </v-flex>
        <v-flex d-flex xs12 md4 style="padding-top:50px">
          <v-card color="grey darken-3" dark class="hidden-sm-and-up">
            <morevideos title="Notícias relacionadas"></morevideos>
          </v-card>
        </v-flex>
      </v-layout>
    </v-container>
    <!-- Fim da primeira grid -->
  </div>
</template>

<script>
import latestnews from '~/components/latestnews'
import morevideos from '~/components/morevideos'
import carroartigo from '~/components/carroartigo'
export default {
  components: {
    latestnews,
    carroartigo,
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
