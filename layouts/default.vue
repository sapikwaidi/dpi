<template>
  <v-app dark>
    <v-navigation-drawer
      v-model="sideDrawer"
      fixed
      app
    >

      <!-- contain sideDrawer -->
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
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <!-- contain -->
    <v-main>
      <v-container fluid>
        <Nuxt />
      </v-container>
    </v-main>

    <v-bottom-navigation 
    fixed
    horizontal
    color="primary"
    height="10vh"
    app>
      <v-app-bar-nav-icon
      @click.stop="sideDrawer = !sideDrawer"
      v-ripple="false"
      plain/>
        <v-btn
        v-for="(item, index) in bottomMenu"
        :key="index"
        :to="item.to"
        v-ripple="false"
        plain>
          <span>{{ item.title }}</span>
          <v-icon>{{ item.icon }}</v-icon>
        </v-btn>
        <v-spacer></v-spacer>
    </v-bottom-navigation>
  </v-app>
</template>

<script>
export default {
  name: 'DefaultLayout',
  data() {
    return {
      
      sideDrawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-application',
          title: 'App',
          to: '/',
        },
        {
          icon: 'mdi-account',
          title: 'Account',
          to: '/account',
        },
      ],
      bottomMenu: [
        {
          icon: 'mdi-application',
          title: 'App',
          to: '/',
        },
      ],
    }
  },
}
</script>
