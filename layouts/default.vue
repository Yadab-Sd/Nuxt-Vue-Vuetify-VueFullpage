<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="drawer"
      class="y-big-shadow"
      :mini-variant="miniVariant"
      app
      permanent
      floating
      stateless
      color="primary"
      height="100%"
    >
      <Logo />
      <MyInfo />
    </v-navigation-drawer>
    <v-app-bar color="primary" class="white--text text--lighten-4 y-big-shadow" clipped-right fixed app>
      <v-app-bar-nav-icon color="accent" @click.stop="drawer = !drawer" />
      <v-btn  icon @click.stop="miniVariant = !miniVariant">
        <v-icon color="accent">mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-toolbar-title class="gradient-txt" v-text="title" />
    </v-app-bar>
    <v-content>
      <nuxt />
    </v-content>
    <v-navigation-drawer
      v-model="drawer"
      mini-variant
      app
      permanent
      floating
      stateless
      clipped
      right
      color="transparent"
      :height="socials.length*48+socials.length*4+16+4"
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in socials"
          :key="i"
          :to="item.to"
          router
          exact
          class="my-1 socials"
          :color="item.color"
        >
          <v-list-item-action>
            <v-icon color="white">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title class="white--text" v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
  </v-app>
</template>

<script>
import Logo from '~/components/Logo.vue'
import MyInfo from '~/components/MyInfo.vue'

export default {
  components: {
    Logo,
    MyInfo
  },
  data() {
    return {
      drawer: true,
      socials: [
        {
          icon: 'mdi-github',
          title: 'Github',
          to: '/',
          color: 'grey'
        },
        {
          icon: 'mdi-stack-overflow',
          title: 'Stackoverflow',
          to: '/',
          color: 'orange'
        },
        {
          icon: 'mdi-quora',
          title: 'Quora',
          to: '/',
          color: 'accent'
        },
        {
          icon: 'mdi-poll',
          title: 'Codeforces',
          to: '/',
          color: 'yellow'
        },
        {
          icon: 'mdi-facebook',
          title: 'Facebook',
          to: '/',
          color: '#0000aa'
        },
        {
          icon: 'mdi-twitter',
          title: 'Twitter',
          to: '/',
          color: 'info'
        },
        {
          icon: 'mdi-linkedin',
          title: 'LinkedIn',
          to: '/',
          color: '#8888ff'
        }
      ],
      miniVariant: false,
      title: 'Yadab Sutradhar'
    }
  }
}
</script>
<style lang="scss" scoped>
  .y-big-shadow {
    box-shadow: 0 0 5px rgba(0,0,0,.8);
  }
  .y-border-b {
    border-bottom: 1px solid $accent;
    border-color: $accent !important;
  }
  .y-border-r {
    border-right: 1px solid $accent;
    border-color: $accent !important;
  }
  .theme--light.v-list-item--active::before {
    opacity: 1;
  }
  .socials:hover {
    width: 246px !important;
  }
  main {
    padding-right: 0 !important;
  }
</style>
