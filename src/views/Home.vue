<template>
  <div class="home">
    <v-container>
      <div class="mt-4">
        <h1 class="text-center">クイズ一覧</h1>
        <h2 class="text-center">新着</h2>
      </div>
    <v-row>
      <v-col
          v-for="(item, i) in items"
          :key="i"
          cols="12"
        >
          <v-card
            :color="item.color"
          >
            <div class="d-flex">
              <v-avatar
                class="ma-3"
                size="125"
                tile
              >
                <v-img :src="item.src"></v-img>
              </v-avatar>
              <div>
                <v-card-title
                  class="headline"
                  v-text="item.title"
                ></v-card-title>

                <v-card-subtitle v-text="item.description"></v-card-subtitle>

                <v-card-actions>
                  <v-btn
                    v-if="item.description === 'Ellie Goulding'"
                    class="ml-2 mt-3"
                    fab
                    icon
                    height="40px"
                    right
                    width="40px"
                  >
                    <v-icon>mdi-play</v-icon>
                  </v-btn>

                </v-card-actions>
              </div>
            </div>
          </v-card>
        </v-col>
      <v-col cols="12">
        <h1 class="text-center mt-4">カテゴリー</h1>
        <v-row>
          <v-col cols="3" v-for="(item,i) in 8" :key="i">
            <v-card>
              <v-img
                src="https://cdn.vuetifyjs.com/images/cards/foster.jpg"
                class="white--text align-end"
                gradient="to bottom, rgba(0,0,0,.1), rgba(0,0,0,.5)"
                height="200px"
              >
              </v-img>
              <v-card-title>カテゴリー名</v-card-title>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from 'vue-property-decorator'

@Component({
  components: {
  },
  data: () => ({
    items: [
      {
        color: '#FFF',
        src: 'https://cdn.vuetifyjs.com/images/cards/foster.jpg',
        title: 'クイズタイトル',
        description: 'クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容'
      },
      {
        color: '#FFF',
        src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
        title: 'クイズタイトル',
        description: 'クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容'
      },
      {
        color: '#FFF',
        src: 'https://cdn.vuetifyjs.com/images/cards/halcyon.png',
        title: 'クイズタイトル',
        description: 'クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容クイズ内容'
      }
    ]
  })
})
export default class Home extends Vue {}
</script>
