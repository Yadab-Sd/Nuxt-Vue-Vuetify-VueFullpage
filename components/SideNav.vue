<template>
  <v-card
    color="transparent"
    class="mx-auto myGray--text"
    tile
    flat
  >
      <v-list class="myGray--text">
        <v-list-item link>
          <v-list-item-content>
            <v-list-item-title v-text="name" class="title white--text">John Leider</v-list-item-title>
            <v-list-item-subtitle v-text="title" class="myGray--text">john@vuetifyjs.com</v-list-item-subtitle>
          </v-list-item-content>

          <v-list-item-action>
            <v-icon>mdi-menu-down</v-icon>
          </v-list-item-action>
        </v-list-item>
      </v-list>
      <v-divider color="myGray"></v-divider>
      <v-list
        nav
        dense
      >
        <v-list-item-group v-model="item" color="myGray">
          <v-list-item
            v-for="(item, i) in sideNav"
            :key="i"
          >
            <v-list-item-icon>
              <v-icon v-text="item.icon" color="myGray"></v-icon>
            </v-list-item-icon>

            <v-list-item-content>
              <v-list-item-title v-text="item.title" class="myGray--text"></v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list-item-group>
      </v-list>
  </v-card>
</template>

<script>
import Logo from '~/components/Logo.vue'

export default {
  components: {
    Logo
  },
  data() {
    return {
      drawer: true,
      item: 0,
      sideNav: [
        {
          icon: 'mdi-github',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-github',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-github',
          title: 'Home',
          to: '/'
        },
        {
          icon: 'mdi-github',
          title: 'Home',
          to: '/'
        }
      ],
      title: 'Programmer',
      name: 'Yadab Sutradhar',
      email: 'yadab.sd2013@gmail.com',
      about: 'Secondary line text Lorem ipsum dolor sit amet, consectetur adipiscing elit.'
    }
  }
}
</script>
