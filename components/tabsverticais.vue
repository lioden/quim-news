<template>
  <v-layout align-center>
    <v-item-group
      v-model="window"
      class="shrink mr-4"
      mandatory
      tag="v-flex"
      style="background:#fff;box-shadow: 2px 2px 8px 2px #b3b3b3b3;"
    >
      <v-item v-for="n in length" :key="n">
        <div slot-scope="{ active, toggle }">
          <v-btn :input-value="active" icon @click="toggle">
            <v-icon>mdi-record</v-icon>
          </v-btn>
        </div>
      </v-item>
    </v-item-group>

    <v-flex>
      <v-window
        v-model="window"
        style="background:#fff;box-shadow: 2px 2px 8px 2px #b3b3b3b3;"
        vertical
      >
        <v-window-item v-for="n in length" :key="n">
          <v-container fill-height>
            <v-flex xs3 raised style="padding-right:5px">
              <v-card style="box-shadow: 2px 2px 8px 2px #b3b3b3b3;">
                <v-img :src="post.image[n]" height="300" flat></v-img>
              </v-card>
            </v-flex>
            <v-flex xs9 style="padding-left:10px">
              <v-card flat>
                <v-card-text>
                  <v-layout align-center mb-3>
                    <v-avatar color="grey" class="mr-3"></v-avatar>
                    <strong class="title">{{ post.title[n - 1] }}</strong>
                    <v-spacer></v-spacer>
                  </v-layout>
                  <p style="font-size:18px">
                    {{ post.text[n - 1] }}
                  </p>
                </v-card-text>
                <div class="text-xs-center" style="padding-bottom:10px">
                  <v-btn color="red darken-3" class="white--text raised">
                    Ler notícia completa
                  </v-btn>
                </div>
                <v-spacer></v-spacer>
              </v-card>
            </v-flex>
          </v-container>
        </v-window-item>
      </v-window>
    </v-flex>
  </v-layout>
</template>

<script>
export default {
  data: () => ({
    image:
      'https://images.unsplash.com/photo-1518780664697-55e3ad937233?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=701&q=80',
    post: {
      title: [
        'Uma cabrita perdeu-se no monte',
        'A maria comprou uma saia nova',
        'Um coelho francês aterroriza as populações de Codal',
        'Um milennial plantou uma leguminosa'
      ],
      text: [
        'Uma cabrita de cor bege foi avistada pela última vez na rua do tanque junto á igreja de Madaíl pelas 23:50 da passada Sexta-Feira. As autoridades prometem encontrar a cabrita o mais rapidamente possível de forma a garantir o mínimo sofrimento por parte do caprino. ',
        'Após 30 anos com a mesma saia na missa, a Maria dos limões comprou uma saia nova. O acontecimento foi reportado ao Senhor Joaquim de imediato pela coruja do bairro.',
        'Momentos emotivos se deram esta manhã na freguesia de codal. As mães escondiam os filhos entre as saias, homens feitos gritavam de forma errónea e idosos ligavam ás companhias de seguros. Corpos militares foram mobilizados ao local de forma a neutralizar a ameaça que era um coelho de origem francesa, de aspeto excessivamente fofo e de profunda amargura emocional.',
        'Em plena Primavera do ano de 2019, foi avistado um milennial com atividades suspeitas numa plantação oliveirense. Á chegada das autoridades ao local, foi concluído que o milennial plantou uma leguminosa com sucesso - com ausência de gritos, danças de vídeos da katy perry com 5 anos e autocarros voadores. O padre Amaro não sabe o que dizer após condenar o jovem no Domingo anterior.'
      ],
      image: [
        'https://images.unsplash.com/photo-1518780664697-55e3ad937233?ixlib=rb-1.2.1&ixid=eyJhcHBfaWQiOjEyMDd9&auto=format&fit=crop&w=701&q=80'
      ]
    },
    length: 4,
    window: 0
  })
}
</script>
