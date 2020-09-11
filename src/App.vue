<template>
  <v-ons-navigator :page-stack="pageStack">
    <component :is="page" v-for="page in pageStack" :key="page.key" :page-stack="pageStack"></component>
  </v-ons-navigator>
</template>

<script>
  import page1 from './Page1';
  import page2 from './Page2';
  import page3 from './Page3';
   import page4 from './Page4';
    import page5 from './Page5';
  
 

  export default {
    data() {
      return {
        pageStack: [page1]
      }
    }
  }
  
</script>
