<template>
  <v-app>

    
    <MyNavBar/>

    <v-main>
      <v-container style="height:100%">
        <MyIndex/>
      </v-container>
    </v-main>

    <v-footer>
      <v-btn color="primary" block>Weiter</v-btn>
    </v-footer>


  </v-app>
</template>

<script>
import MyNavBar from './components/templates/MyNavBar';
import MyIndex from './components/views/MyIndex';
// import MyIndexModal from './components/modals/MyIndexModal';




export default {
  name: 'App',

  components: {
    MyNavBar,
    MyIndex,
    // MyIndexModal,
  },

  data: () => ({
    //
  }),
};
</script>
