<template>
    <v-container>

        <v-text-field class="m-0 p-0" hide-details label="Abfahrt" placeholder="Abfahrt" outlined></v-text-field>
        <v-text-field class="m-0 p-0"  label="Ankunft" placeholder="Ankunft" outlined></v-text-field>


        <v-btn elevation="2" style="width:50%" color="primary">Abfarht</v-btn>
        <v-btn elevation="2" style="width:50%">Ankunft</v-btn>

        <v-text-field   label="Uhrzeit" placeholder="Uhrzeit" outlined></v-text-field>


        <v-dialog width="500" class="p-4 m-4">
        <template v-slot:activator="{ on, attrs }">
          <v-btn block v-bind="attrs" v-on="on">
            Bus 83 | 08:00 - 09:11
          </v-btn>
        </template>
  
        <v-card>
          <v-card-title class="text-h5 grey lighten-2">
            Bus 83 | 08:00 - 09:11
          </v-card-title>
  
          <v-card-text>
            <v-btn small width="10%">2x</v-btn>
            <v-btn small width="45%">3,1€ Normal</v-btn>
            <v-btn small width="10%">+</v-btn>
            <v-btn small width="10%">-</v-btn>

            <v-btn small width="10%">2x</v-btn>
            <v-btn small width="45%">3,1€ Normal</v-btn>
            <v-btn small width="10%">+</v-btn>
            <v-btn small width="10%">-</v-btn>

            <v-btn small width="10%">2x</v-btn>
            <v-btn small width="45%">3,1€ Normal</v-btn>
            <v-btn small width="10%">+</v-btn>
            <v-btn small width="10%">-</v-btn>
          </v-card-text>
  
          <v-divider></v-divider>
  
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" block>Schließen</v-btn>
          </v-card-actions>
        </v-card>
        </v-dialog>

        <v-dialog width="500" class="p-4 m-4">
        <template v-slot:activator="{ on, attrs }">
          <v-btn block v-bind="attrs" v-on="on" class="text-left">
            Bus 42 | 10:15 - 11:15
          </v-btn>
        </template>
  
        <v-card>
          <v-card-title class="text-h5 grey lighten-2">
            Bus 42 | 10:15 - 11:15
          </v-card-title>
  
          <v-card-text>
            <v-btn small width="10%">2x</v-btn>
            <v-btn small width="45%">3,1€ Normal</v-btn>
            <v-btn small width="10%">+</v-btn>
            <v-btn small width="10%">-</v-btn>

            <v-btn small width="10%">2x</v-btn>
            <v-btn small width="45%">3,1€ Normal</v-btn>
            <v-btn small width="10%">+</v-btn>
            <v-btn small width="10%">-</v-btn>

            <v-btn small width="10%">2x</v-btn>
            <v-btn small width="45%">3,1€ Normal</v-btn>
            <v-btn small width="10%">+</v-btn>
            <v-btn small width="10%">-</v-btn>
          </v-card-text>
  
          <v-divider></v-divider>
  
          <v-card-actions>
            <v-spacer></v-spacer>
             <v-btn color="primary" block>Schließen</v-btn>
          </v-card-actions>
        </v-card>
        </v-dialog>

        
    </v-container>
</template>

<!-- 
<template>
    <v-container>
        <v-text-field class="m-0 p-0" hide-details label="Auftragsübersicht" placeholder="Auftragsübersicht" outlined></v-text-field>
        <br>
        <v-btn small width="10%" height="60px">2x</v-btn>
        <v-btn small width="54%" height="60px">Bus 83 | 08:16 - 09:11<br>Trier Süd - Trier West <br>3,1 € Normal</v-btn>
        <v-btn small width="10%" height="60px">+</v-btn>
        <v-btn small width="10%" height="60px">-</v-btn>

        <v-btn small width="10%" height="60px">2x</v-btn>
        <v-btn small width="54%" height="60px">Bus 83 | 08:16 - 09:11<br>Trier Süd - Trier West <br>3,1 € Normal</v-btn>
        <v-btn small width="10%" height="60px">+</v-btn>
        <v-btn small width="10%" height="60px">-</v-btn>
        

    </v-container>
</template> -->