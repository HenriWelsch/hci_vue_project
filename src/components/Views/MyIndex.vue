<template>
    <v-container>

        <v-text-field label="Abfahrt" placeholder="Abfahrt" outlined></v-text-field>
        <v-text-field label="Ankunft" placeholder="Ankunft" outlined></v-text-field>
        <v-text-field label="Uhrzeit" placeholder="Uhrzeit" outlined></v-text-field>

        <template v-slot:activator="{ on, attrs }">
          <v-btn
            block
            v-bind="attrs"
            v-on="on"
          >
            Von hier nach da
          </v-btn>
        </template>

    </v-container>
</template>