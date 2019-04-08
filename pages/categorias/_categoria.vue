<template>
  <div>
    <!-- Primeira Grid -->
    <v-container fluid grid-list-xl class="pa-0">
      <div class="customtitle text-xs-center text-capitalize">
        {{ identificador }}
      </div>
      <br />
      <v-layout row wrap>
        <v-flex d-flex xs12 md8>
          <v-layout row wrap>
            <v-flex d-flex xs12 md12>
              <v-card color="red darken-2" dark height="525px">
                <carro
                  :titles="titles"
                  :identificadores="blocoids"
                  :sources="blocourls"
                ></carro>
              </v-card>
            </v-flex>
            <v-flex d-flex xs12 md6>
              <v-layout row wrap>
                <v-flex d-flex xs6 md12>
                  <cardlandscape
                    class="hoverable"
                    :title="titles[0]"
                    :image="blocourls[0]"
                  ></cardlandscape>
                </v-flex>
                <v-flex d-flex xs6 md12>
                  <cardlandscapeinv
                    class="hoverable"
                    :title="titles[1]"
                    :image="blocourls[1]"
                  ></cardlandscapeinv>
                </v-flex>
              </v-layout>
            </v-flex>
            <v-flex d-flex xs12 md6>
              <iframe
                width="100%"
                height="100%"
                src="https://www.youtube.com/embed/R_uS0aT0bG8"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </v-flex>
            <v-flex d-flex xs12 md12>
              <v-card color="transparent" dark height="400">
                <v-img
                  style="min-height:300px;max-height:300px"
                  :src="blocourls[4]"
                ></v-img>
                <v-card-text class="headline text-capitalize">{{
                  titles[4]
                }}</v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 md4>
          <latestnews :titles="titles" :images="blocourls"></latestnews>
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
        <v-flex d-flex xs1 md1 class="potato"
          ><div class="arrowleft bounceleft" @click="previousvideo"></div
        ></v-flex>
        <v-flex d-flex xs10 md10>
          <v-layout row wrap>
            <v-flex d-flex xs12 md12>
              <iframe
                width="100%"
                height="500px"
                :src="video"
                frameborder="0"
                allow="accelerometer; autoplay; encrypted-media; gyroscope; picture-in-picture"
                allowfullscreen
              ></iframe>
            </v-flex>
            <v-flex d-flex xs12 md12>
              <v-layout row wrap>
                <v-flex d-flex xs12 md12>
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
        <v-flex d-flex xs1 md1 class="potato"
          ><div class="arrowright bounceright" @click="nextvideo"></div
        ></v-flex>
      </v-layout>
      <br />
      <p class="text-xs-center grey--text caption">
        Icons made by
        <a href="https://www.freepik.com/" title="Freepik">Freepik</a> from
        <a href="https://www.flaticon.com/" title="Flaticon"
          >www.flaticon.com</a
        >
        is licensed by
        <a
          href="http://creativecommons.org/licenses/by/3.0/"
          title="Creative Commons BY 3.0"
          target="_blank"
          >CC 3.0 BY</a
        >
      </p>
    </v-container>
    <!-- Fim da segunda grid -->
    <br />
    <hr />
    <br />
  </div>
</template>

<script>
import latestnews from '~/components/latestnews'
import cardlandscape from '~/components/card-landscape'
import cardlandscapeinv from '~/components/card-landscape-inverted'
import carro from '~/components/carro'
import axios from 'axios'
export default {
  components: {
    latestnews,
    cardlandscape,
    cardlandscapeinv,
    carro
  },
  data: () => ({
    nvideo: 0,
    video: 'https://www.youtube.com/embed/R_uS0aT0bG8',
    videos: [
      'https://www.youtube.com/embed/R_uS0aT0bG8',
      'https://www.youtube.com/embed/bX3dwi_yuSA',
      'https://www.youtube.com/embed/FuP_hNi-UPY'
    ],
    blocourls: [],
    titles: [],
    blocoids: [],
    array: [],
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
      'https://images.unsplash.com/photo-1553643182-15d168e4d680?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=634&q=80',
    identificador: ''
  }),
  created: function() {
    this.identificador = this.$route.params.categoria
    this.pedido(this.identificador)
  },
  methods: {
    pedido: function(categoria) {
      const self = this
      self.blocourls = []
      self.blocoids = []
      self.titles = []
      axios
        .get(
          'https://api.unsplash.com/search/photos/?page=1;query=' +
            categoria +
            ';client_id=2ebf903d65d58846dba610108cbf428043756525989c37bfd1121174ff28a339'
        )
        .then(function(response) {
          self.array = []
          self.array.push(response)
          for (const index in self.array[0].data.results) {
            self.blocourls.push(self.array[0].data.results[index].urls.regular)
            self.blocoids.push(self.array[0].data.results[index].id)
            self.titles.push(self.array[0].data.results[index].alt_description)
          }
        })
        .catch(function(error) {
          console.log(error)
        })
    },
    nextvideo: function() {
      this.nvideo = this.nvideo + 1
      this.video = this.videos[this.nvideo]
    },
    previousvideo: function() {
      if (this.nvideo > 0) {
        this.nvideo = this.nvideo - 1
      }
      this.video = this.videos[this.nvideo]
    }
  }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Teko');
a {
  color: #d0d0d0;
  text-decoration: none; /* no underline */
}
.potato {
  margin-top: 20%;
  background-color: transparent;
  height: 100px;
  width: 10px;
}
.potato:hover {
  border-style: solid;
  border-width: 1px;
  border-radius: 10px;
}
.transparent {
  background-color: black !important;
  opacity: 0.9;
  border-color: transparent !important;
}
.arrowright {
  position: relative;
  top: 25%;
  left: 60%;
  margin-left: -30px;
  height: 40px;

  /**
   * Dark Arrow Down
   */
  background-image: url(https://image.flaticon.com/icons/png/512/55/55149.png);
  background-size: contain;
}
.arrowleft {
  position: relative;
  top: 25%;
  left: 40%;
  margin-left: -10px;
  height: 40px;

  /**
   * Dark Arrow Down
   */
  background-image: url(https://image.flaticon.com/icons/png/512/61/61752.png);
  background-size: contain;
}

.bounceright {
  animation: bounceright 2s infinite;
}

@keyframes bounceright {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateX(0);
  }
  40% {
    transform: translateX(5px);
  }
  60% {
    transform: translateX(2px);
  }
}
.bounceleft {
  animation: bounceleft 2s infinite;
}

@keyframes bounceleft {
  0%,
  20%,
  50%,
  80%,
  100% {
    transform: translateX(0);
  }
  40% {
    transform: translateX(-5px);
  }
  60% {
    transform: translateX(-2px);
  }
}

.customtitle {
  font-family: 'Teko', sans-serif;
  font-size: 40px;
}
.hoverable:hover {
  transform: scale(1.02);
  cursor: pointer;
}
</style>
