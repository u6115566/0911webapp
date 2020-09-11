<style scoped>
      
        .loginform {
            text-align: center;
            margin-bottom:30px;
          margin-bottom:30px;
        }
        .catch{
          color:#565E97;
          font-weight:bold;
          margin-bottom:30px;
          margin-bottom:30px;
        }
        .apptitle{
          color:#565E97;
          font-weight:bold;
          margin-bottom:30px;
          margin-bottom:30px;
        }
        .logo{
          margin-top:50px;
        }
        input{
          margin-bottom:30px;
          margin-bottom:30px;
        }
        v-ons-button{
          background-color: ##FBC1B5;
          color: #707070;
          border-radius: 10px;
          margin-left:30px;
          margin-right:30px;
        };
</style>
<template id="signup">
  <v-ons-page>

    <!-- <custom-toolbar>ログイン</custom-toolbar> -->
    <div class="loginform">
     <img class="logo" src="../public/logo.png" alt="">
     
        <p class="catch">推しを見逃さないカレンダーアプリ</p> 
  <h1 class="apptitle">おたカレ</h1>
    <form method="post" action="">
          <input  type="text" name="name"><br>
        <input type="password" name="pass">
        </form>
      <v-ons-button @click="push">新規登録</v-ons-button>
      <v-ons-button @click="push2">ログイン</v-ons-button>
    </div>
  </v-ons-page>
</template> 

<script>
  import customToolbar from './CustomToolbar';
  import page2 from './Page2';
    import page5 from './Page5';
  
  export default {
     methods: {
       pop(){
         this.pageStack.pop();
       },
       push() {
         this.pageStack.push(page2);
       },
       push2() {
         this.pageStack.push(page5);
       },
       
     },
     props: ['pageStack'],
     components: { customToolbar },
     key: 'key_page1',
  }
</script>

<!-- <style scoped>
      
        .loginform {
            text-align: center;
            margin-bottom:30px;
          margin-bottom:30px;
        }
        .catch{
          color:#565E97;
          font-weight:bold;
          margin-bottom:30px;
          margin-bottom:30px;
        }
        .apptitle{
          color:#565E97;
          font-weight:bold;
          margin-bottom:30px;
          margin-bottom:30px;
        }
        .logo{
          margin-top:50px;
        }
        input{
          margin-bottom:30px;
          margin-bottom:30px;
        }
        v-ons-button{
          background-color: ##FBC1B5;
          color: #707070;
          border-radius: 10px;
          margin-left:30px;
          margin-right:30px;
        };
</style>-->