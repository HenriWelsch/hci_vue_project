<template>
  <v-app>

    
    <MyNavBar/>

    <v-main>
      <v-container style="height:100%">

        <div v-if="side1">
          <v-text-field class="m-0 p-0" hide-details label="Abfahrt" placeholder="Abfahrt" outlined></v-text-field>
          <v-text-field class="m-0 p-0"  label="Ankunft" placeholder="Ankunft" outlined></v-text-field>
          
          <div v-if="toggler">
            <v-btn elevation="2" style="width:50%" color="primary">Abfarht</v-btn>
            <v-btn @click="toggler = !toggler" elevation="2" style="width:50%">Ankunft</v-btn>
            <v-text-field label="Uhrzeit Abfahrt" placeholder="Uhrzeit Abfahrt" outlined></v-text-field>
          </div>
          <div v-else>
            <v-btn @click="toggler = !toggler" elevation="2" style="width:50%">Abfarht</v-btn>
            <v-btn elevation="2" style="width:50%" color="primary">Ankunft</v-btn>
            <v-text-field label="Uhrzeit Ankunft" placeholder="Uhrzeit Ankunft" outlined></v-text-field>
          </div>

          <v-btn block color="primary"  @click="suche = !suche">Suchen</v-btn>

          <div v-if="suche">
            <!-- Hierbei handelt es sich um den start eines Modals -->
            <v-dialog width="500" class="p-4 m-4">
              <template v-slot:activator="{ on, attrs }">
                <v-btn block v-bind="attrs" v-on="on">Bus 83 | 08:00 - 09:11</v-btn>
              </template>

              <v-card>
                <v-card-title class="text-h5 grey lighten-2">Bus 83 | 08:00 - 09:11</v-card-title>

                <v-card-text>
                  <br>
                  <v-btn small width="10%">{{counter1}}x</v-btn>
                  <v-btn small width="45%">3,1€ Normal</v-btn>
                  <v-btn @click="counter1++" small width="10%">+</v-btn>
                  <v-btn @click="(counter1 == 0) ? 0 : counter1--" small width="10%">-</v-btn>

                  <v-btn small width="10%">{{counter2}}x</v-btn>
                  <v-btn small width="45%">3,1€ Kinder</v-btn>
                  <v-btn @click="counter2++" small width="10%">+</v-btn>
                  <v-btn @click="(counter2 == 0) ? 0 : counter2--" small width="10%">-</v-btn>

                  <v-btn small width="10%">{{counter3}}x</v-btn>
                  <v-btn small width="45%">3,1€ Senioren</v-btn>
                  <v-btn @click="counter3++" small width="10%">+</v-btn>
                  <v-btn @click="(counter3 == 0) ? 0 : counter3--" small width="10%">-</v-btn>
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                  <v-spacer></v-spacer>
                  <v-btn color="primary" block>Schließen</v-btn>
                </v-card-actions>
              </v-card>
            </v-dialog>
            <!-- Hierbei handelt es sich um das ende eines Modals -->


            <v-btn block v-bind="attrs" v-on="on" class="text-left">Bus 42 | 10:15 - 11:15</v-btn>
            <v-btn block v-bind="attrs" v-on="on" class="text-left">Bus 42 | 10:15 - 11:15</v-btn>
            <v-btn block v-bind="attrs" v-on="on" class="text-left">Bus 42 | 10:15 - 11:15</v-btn>
          </div>



        </div>
        <div v-else>
          <v-text-field class="m-0 p-0" hide-details label="Auftragsübersicht" placeholder="Auftragsübersicht" outlined></v-text-field>
          <br>
          <div v-if="counter1 != 0">
            <v-btn small width="10%" height="60px">{{counter1}}x</v-btn>
            <v-btn small width="57%" height="60px">Bus 83 | 08:16 - 09:11<br>Trier Süd - Trier West <br>3,1 € Normal</v-btn>
            <v-btn small width="10%" height="60px" @click="counter1++">+</v-btn>
            <v-btn small width="10%" height="60px" @click="(counter1 == 0) ? 0 : counter1--">-</v-btn>
          </div>

          <div v-if="counter2 != 0">
            <v-btn small width="10%" height="60px">{{counter2}}x</v-btn>
            <v-btn small width="57%" height="60px">Bus 83 | 08:16 - 09:11<br>Trier Süd - Trier West <br>3,1 € Kinder</v-btn>
            <v-btn small width="10%" height="60px" @click="counter2++">+</v-btn>
            <v-btn small width="10%" height="60px" @click="(counter2 == 0) ? 0 : counter2--">-</v-btn>
          </div>

          <div v-if="counter3 != 0">
            <v-btn small width="10%" height="60px">{{counter3}}x</v-btn>
            <v-btn small width="57%" height="60px">Bus 83 | 08:16 - 09:11<br>Trier Süd - Trier West <br>3,1 € Senioren</v-btn>
            <v-btn small width="10%" height="60px" @click="counter3++">+</v-btn>
            <v-btn small width="10%" height="60px" @click="(counter3 == 0) ? 0 : counter3--">-</v-btn>
          </div>

        </div>


        

        

      </v-container>
    </v-main>

    <v-footer v-if="side1">
      <v-btn @click="side1 = !side1" color="primary" block>Weiter</v-btn>
    </v-footer>
    <v-footer v-else>
      <v-btn  @click="side1 = !side1" elevation="2" style="width:50%" color="primary">Zurück</v-btn>

      <v-dialog width="500" class="p-4 m-4">
            <template v-slot:activator="{ on, attrs }">
              <v-btn v-bind="attrs" v-on="on" elevation="2" style="width:50%" color="primary">Zahlen</v-btn>

            </template>

            <v-card>
              <v-card-title class="text-h5 grey lighten-2">Bus 83 | 08:00 - 09:11</v-card-title>

              <v-card-text>
                <br>
                <v-btn block>Bar</v-btn>
                <v-btn block>Visa</v-btn>
                <v-btn block>Debit Card</v-btn>
                <v-btn block>Apple Pay</v-btn>
              </v-card-text>

              <v-divider></v-divider>

              <v-card-actions>
                <v-spacer></v-spacer>
                <v-btn elevation="2" style="width:50%" color="primary">Zurück</v-btn>
                <v-btn elevation="2" style="width:50%" color="primary">Zahlen</v-btn>
              </v-card-actions>
            </v-card>
          </v-dialog>
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




export default {
  name: 'App',

  components: {
    MyNavBar,
  },

  data: () => ({
    suche:false,
    side1:true,
    toggler:true,
    text: true,
    counter1:0,
    counter2:0,
    counter3:0,
  }),

  methods : {
    toggleSwitches() {
      this.toggler = !this.toggler
    }
  }

};
</script>
