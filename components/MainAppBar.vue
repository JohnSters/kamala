<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
      color="#0E2634"
    >
      <v-img src="/logo.png" max-width="200" class="hidden-md-and-up ma-auto mt-3"></v-img>
      <v-divider class="ma-3 white"></v-divider>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          class="white--text"
          router
          exact
        >
          <v-list-item-action>
            <v-icon color="white">{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      height="120"
      color="#0E2634"
      flat
      fixed
      app
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-md-and-up" dark />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
      </v-btn>
      <v-img src="/logo.png" max-width="350" class="hidden-sm-and-down"></v-img>
      <v-img src="/logo.png" max-width="230" class="hidden-md-and-up ml-n4"></v-img>
      <v-spacer />
      <v-btn class="white--text text-capitalize hidden-sm-and-down" rounded text>Be</v-btn>
      <v-btn class="white--text text-capitalize hidden-sm-and-down" rounded text>Grow</v-btn>
      <v-btn class="white--text text-capitalize hidden-sm-and-down" rounded text>Learn</v-btn>
      <v-btn class="white--text text-capitalize hidden-sm-and-down" rounded text>Book</v-btn>
      <v-btn class="white--text text-capitalize hidden-sm-and-down" rounded text>Attend</v-btn>
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: 'MainAppBar',
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-yoga',
          title: 'Be',
          to: '/'
        },
        {
          icon: 'mdi-yoga',
          title: 'Grow',
          to: '/'
        },
        {
          icon: 'mdi-yoga',
          title: 'Learn',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Book',
          to: '/inspire'
        },
        {
          icon: 'mdi-yoga',
          title: 'Attend',
          to: '/'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style scoped>

</style>
