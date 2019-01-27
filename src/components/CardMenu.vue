<template>
  <v-layout align-start justify-center row>
    <v-flex v-for="( sample, i ) in samples" :key="`4${i}`">
      <v-card max-width="300px">
        <v-img
          class="white--text"
          height="100px"
          :src="sample.image"
        >
          <v-container fill-height fluid>
            <v-layout fill-height>
              <v-flex xs12 align-end flexbox>
                <span class="headline">{{ sample.headline }}</span>
              </v-flex>
            </v-layout>
          </v-container>
        </v-img>
        <v-card-title>
          <div>
            <span class="grey--text">{{ sample.title}}</span><br>
            <span>{{ sample.description1 }}</span><br>
            <span>{{ sample.description2 }}</span><br>
            <span>{{ sample.description3 }}</span>
          </div>
        </v-card-title>
        <v-card-actions>
          <v-btn flat color="orange">見る</v-btn>
        </v-card-actions>
      </v-card>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    data: () => ({
      samples: [
        {
          headline: 'GoogleMapサンプル',
          title: 'GoogleMapサンプル',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
          image: 'https://cdn.vuetifyjs.com/images/cards/desert.jpg',
          description1: '美容院・理髪店などでの予約からアフターフォローまで',
          description2: '整備工場・ガソリンスタンドなどでの入庫予約から納車後のフォローまで',
          description3: 'ドラッグ＆ドロップで情報のステータスや担当者を変更出来ます。'
        },
        {
          headline: 'Trello風な案件管理',
          title: 'Trello風な案件管理',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
          image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
          description1: '美容院・理髪店などでの予約からアフターフォローまで',
          description2: '整備工場・ガソリンスタンドなどでの入庫予約から納車後のフォローまで',
          description3: 'ドラッグ＆ドロップで情報のステータスや担当者を変更出来ます。'
        },
        {
          headline: 'Trello風な案件管理',
          title: 'Trello風な案件管理',
          href: 'https://github.com/vuetifyjs/vuetify-loader',
          image: 'https://cdn.vuetifyjs.com/images/cards/docks.jpg',
          description1: '美容院・理髪店などでの予約からアフターフォローまで',
          description2: '整備工場・ガソリンスタンドなどでの入庫予約から納車後のフォローまで',
          description3: 'ドラッグ＆ドロップで情報のステータスや担当者を変更出来ます。'
        }
      ]
    })
  }
</script>

<style>

</style>
