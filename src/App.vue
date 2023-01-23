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
<!-- 
    <v-footer>
      <v-btn elevation="2" style="width:50%" color="primary">Ticket Hinzufügen</v-btn>
      

      <v-dialog width="500" class="p-4 m-4">
        <template v-slot:activator="{ on, attrs }">
          <v-btn v-bind="attrs" v-on="on" class="text-left" style="width:50%" color="primary">8,2€ Zahlen</v-btn>
        </template>
  
        <v-card>
          <v-card-title class="text-h5 grey lighten-2">
            Zahlung
          </v-card-title>
          <br>
  
          <v-card-text>
            <v-btn block>Bar</v-btn>
            <v-btn block>Visa</v-btn>
            <v-btn block>Debit Card</v-btn>
            <v-btn block>Apple Pay</v-btn>
          </v-card-text>
  
          <v-divider></v-divider>
  
          <v-card-actions>
            <v-spacer></v-spacer>
             <v-btn width="50%" color="primary" >Schließen</v-btn>
             <v-btn width="50%" color="primary" >zahlen und<br>Ticket drucken</v-btn>
          </v-card-actions>
        </v-card>
        </v-dialog>



    </v-footer> -->


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
