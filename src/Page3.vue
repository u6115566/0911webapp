<template>
  <v-ons-page>
    <!--<custom-toolbar :back-label="'Page 3'">ユーザ登録</custom-toolbar> -->
    <div class="touroku">
    <form method="post" action="">
            <p>ニックネーム： <input type="text" name="name"></p>
            <p>ユーザー名： <input type="text" name="name"></p>
            <p>パスワード： <input type="password" name="pass"></p>
        </form>
        <v-ons-button @click="push2">登録</v-ons-button>
        </div>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';
  import app from './App';
  import page4 from './Page4';

  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      } ,
      push2() {
         this.pageStack.push(page4);
       }
    },
    props: ['pageStack'],
    components: { customToolbar },
    key: 'key_page3',
  }
</script>
<style scoped>
      
        .touroku {
            text-align: center;
        }

        h2{
          color:#565E97;
          font-weight:bold;
          margin:0;
        }
        .apptitle{
          color:#565E97;
          font-weight:bold;
          margin:0;
        }
</style>