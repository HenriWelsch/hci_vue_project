<template>
  <v-app>
    <MyNavBar/>
    <v-main>
      <HelloWorld/>
    </v-main>
  </v-app>
</template>

<script>
import HelloWorld from './components/Views/HelloWorld';
import MyNavBar from './components/templates/MyNavBar';


export default {
  name: 'App',

  components: {
    HelloWorld,
    MyNavBar,
  },

  data: () => ({
    //
  }),
};
</script>
