<template>
  <v-app>
    <MyNavBar/>
    <v-main>
      <v-container>
        <MyIndex/>

        <MyIndexModal/>
        <MyIndexModal/>
        <MyIndexModal/>

      </v-container>

    </v-main>
  </v-app>
</template>

<script>
import MyNavBar from './components/templates/MyNavBar';
import MyIndex from './components/views/MyIndex';
import MyIndexModal from './components/modals/MyIndexModal';




export default {
  name: 'App',

  components: {
    MyNavBar,
    MyIndex,
    MyIndexModal,
  },

  data: () => ({
    //
  }),
};
</script>
