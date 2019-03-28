<template>
  <v-card class="mx-auto" color="#26c6da" dark>
    <v-card-title>
      <v-icon large left>
        local_florist
      </v-icon>
      <span class="title font-weight-light">Crise das couves</span>
    </v-card-title>

    <v-card-text class="headline font-weight-bold">
      Devido aos recentes ardumes na localidade de Pinheiro da Bemposta, há uma
      crescente ausência de couves no mercado, causando o caos entre as avós.
    </v-card-text>

    <v-card-actions>
      <v-list-tile class="grow">
        <v-list-tile-avatar color="grey darken-2">
          <v-img
            class="elevation-6"
            src="https://avataaars.io/?avatarStyle=Transparent&topType=ShortHairSides&accessoriesType=Blank&hairColor=Black&facialHairType=BeardMagestic&facialHairColor=Black&clotheType=Overall&clotheColor=Black&eyeType=Surprised&eyebrowType=FlatNatural&mouthType=Disbelief&skinColor=Light"
          ></v-img>
        </v-list-tile-avatar>

        <v-list-tile-content>
          <v-list-tile-title>Senhor Joaquim</v-list-tile-title>
        </v-list-tile-content>

        <v-layout align-center justify-end>
          <v-icon class="mr-1">mdi-heart</v-icon>
          <span class="subheading mr-2">256</span>
          <span class="mr-1">·</span>
          <v-icon class="mr-1">mdi-share-variant</v-icon>
          <span class="subheading">45</span>
        </v-layout>
      </v-list-tile>
    </v-card-actions>
  </v-card>
</template>

<script>
export default {
  data: () => ({
    //
  })
}
</script>
