<template>
  <v-app>
    <MyNavBar/>
    <v-main>
      <MyIndex/>
    </v-main>
  </v-app>
</template>

<script>
import MyNavBar from './components/templates/MyNavBar';
import MyIndex from './components/views/MyIndex';



export default {
  name: 'App',

  components: {
    MyNavBar,
    MyIndex,
  },

  data: () => ({
    //
  }),
};
</script>
