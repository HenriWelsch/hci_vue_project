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
            Bus 42 10:15 11:15
          </v-card-title>
  
          <v-card-text>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          </v-card-text>
  
          <v-divider></v-divider>
  
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" text>
              I accept
            </v-btn>
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
            Privacy Policy
          </v-card-title>
  
          <v-card-text>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
          </v-card-text>
  
          <v-divider></v-divider>
  
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" text>
              I accept
            </v-btn>
          </v-card-actions>
        </v-card>
        </v-dialog>

        
    </v-container>
</template>