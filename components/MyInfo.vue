<template>
  <v-card
    class="mx-auto myGray--text"
    color="transparent"
    tile
    flat
    inset
  >
    <v-list two-line dense>
      <v-list-item @click="">
        <v-list-item-icon>
          <v-icon color="indigo">mdi-phone</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title class="gradient-txt font-weight-bold">(+88) 01733-267990</v-list-item-title>
          <v-list-item-subtitle class="myGray--text font-weight-light">Mobile</v-list-item-subtitle>
        </v-list-item-content>

        <v-list-item-icon>
          <v-icon color="accent">mdi-message-text</v-icon>
        </v-list-item-icon>
      </v-list-item>

      <v-divider inset></v-divider>

      <v-list-item @click="">
        <v-list-item-icon>
          <v-icon color="indigo">mdi-email</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title class="gradient-txt font-weight-bold">yadab.sd2013@gmail.com</v-list-item-title>
          <v-list-item-subtitle class="myGray--text font-weight-light">Personal</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider inset></v-divider>

      <v-list-item @click="">
        <v-list-item-icon>
          <v-icon color="indigo">mdi-map-marker</v-icon>
        </v-list-item-icon>

        <v-list-item-content>
          <v-list-item-title class="gradient-txt font-weight-300">A-1/5, Sikder Manjeel</v-list-item-title>
          <v-list-item-subtitle class="myGray--text font-weight-light">Khilkhet, Dhaka-1230</v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>
    </v-list>
  </v-card>
</template>