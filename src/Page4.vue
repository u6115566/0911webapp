<template>
  <v-ons-page>
     <!-- <custom-toolbar :back-label="'Page 3'">ログイン成功</custom-toolbar> -->
     <div class="kiyaku">
       <img src="public/logo.png" alt="">
    <p style="text-align: center">ユーザー登録成功しました<br>おめでとうございます</p>
     <v-ons-button @click="push">ログイン</v-ons-button>
     </div>
  </v-ons-page>
</template>
<script>
  
    import customToolbar from './CustomToolbar';
  import app from './App';
  import page1 from './Page1';

  export default {
    methods: {
      pop() {
        this.pageStack.pop();
      } ,
      push() {
         this.pageStack.push(page1);
       }
    },
    props: ['pageStack'],
    components: { customToolbar },
    key: 'key_page3',
  }
  </script>
  <style scoped>
      
        .kiyaku {
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
        .un{

        }
        .pw{

        }
        .signb{
          background-color: ##FBC1B5;
          color: #707070;
          border-radius: 10px;
        }
        .loginb{
          background-color: ##FBC1B5;
          color: #707070;
          border-radius: 10px;
        }
</style>