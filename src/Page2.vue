<template>
  <v-ons-page>
    <!--<custom-toolbar>利用規約</custom-toolbar> -->
    <div class="kiyaku">
    
        <h2>アプリ利用規約</h2>
            <p> 利用規約～～ </p> 
            <input type="checkbox" id="checkbox" v-model="checked">
             <label for="checkbox">{{ checked }}利用規約に同意します</label>
    <br>
      <v-ons-button @click="push">同意して次へ</v-ons-button>
    </p>
    </div>
  </v-ons-page>
</template>

<script>
  import customToolbar from './CustomToolbar';
  import page3 from './Page3';
  export default {
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(page3);
       }
     },
     props: ['pageStack'],
     components: { customToolbar },
     key: 'key_page2',
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
        label{
          margin-bottom:30px;
          margin-bottom:30px;
        }
        .signb{
          background-color: ##FBC1B5;
          color: #707070;
          border-radius: 10px;
          margin-left:30px;
          margin-right:30px;
        }
</style>