<template>
  <div>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
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
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="hidden-md-and-up" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
      </v-btn>
      <v-img src="/logo.png" max-width="350"></v-img>
      <v-spacer />
      <v-btn class="white--text" rounded text>Be</v-btn>
      <v-btn class="white--text" rounded text>Grow</v-btn>
      <v-btn class="white--text" rounded text>Learn</v-btn>
      <v-btn class="white--text" rounded text>Book</v-btn>
      <v-btn class="white--text" rounded text>Attend</v-btn>
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
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
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
