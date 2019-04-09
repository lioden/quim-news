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
              <carro :images="banners" :titles="bannertitles"></carro>
            </v-flex>
            <v-flex d-flex xs12 md6>
              <v-layout row wrap>
                <v-flex d-flex xs6 md12>
                  cardlandscape aqui
                </v-flex>
                <v-flex d-flex xs6 md12>
                  cardlandscapeinv aqui
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
            <v-flex d-flex xs6 md6>
              <v-card color="#2e7d32" dark class="hoverable">
                <v-img style="height:550px" :src="image"></v-img>
                <v-card-text class="headline text-capitalize">
                  titulo do card
                </v-card-text>
              </v-card>
            </v-flex>
            <v-flex d-flex xs6 md6>
              <v-card color="#6a1b9a" dark class="hoverable">
                <v-img style="height:550px" :src="image"></v-img>
                <v-card-text class="headline text-capitalize">
                  Titulo do card
                </v-card-text>
              </v-card>
            </v-flex>
          </v-layout>
        </v-flex>
        <v-flex d-flex xs12 md4>
          latestnewsaqui
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
        <v-flex d-flex xs1 md1 class="mybutton hoverable"
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
        <v-flex d-flex xs1 md1 class="mybutton hoverable"
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
import axios from 'axios'
import carro from '~/components/carro'
export default {
  components: { carro },
  data: () => ({
    banners: [],
    bannertitles: [],
    nvideo: 0,
    video: 'https://www.youtube.com/embed/R_uS0aT0bG8',
    videos: [
      'https://www.youtube.com/embed/R_uS0aT0bG8',
      'https://www.youtube.com/embed/bX3dwi_yuSA',
      'https://www.youtube.com/embed/FuP_hNi-UPY'
    ],
    array: [],
    image:
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
      self.banners = []
      self.bannertitles = []
      self.array = []
      axios
        .get('http://gateway.loba.pt:3001/rest/banners/pt/' + categoria)
        .then(function(response) {
          self.array = response.data.banners
          for (const index in self.array) {
            self.banners.push(self.array[index].image_desktop)
            self.bannertitles.push(self.array[index].title)
          }
          console.log(self.banners)
          console.log(self.bannertitles)
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
.mybutton {
  margin-top: 20%;
  background-color: transparent;
  height: 100px;
  width: 10px;
}
.mybutton:hover {
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
  z-index: 2;
  transform: scale(1.04);
  cursor: pointer;
}
</style>
