<template>
  <v-app id="inspire">
   <v-navigation-drawer 
   v-model="drawer"
   app
   >
      <v-list-item>
        <v-list-item-content>
          <v-list-item-title class="title">
            Menu
          </v-list-item-title>
          <!-- <v-list-item-subtitle>
            subtext
          </v-list-item-subtitle> -->
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>

      <v-list
        dense
        nav
      >
        <v-list-item
          v-for="item in items"
          :key="item.title"
          :to="item.to"
          link
        >
          <v-list-item-icon>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-icon>

          <v-list-item-content>
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app>
      <v-app-bar-nav-icon @click="drawer = !drawer"></v-app-bar-nav-icon>

      <v-toolbar-title>Demonyiaable</v-toolbar-title>
    </v-app-bar>

    <v-main>
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
  export default {
    data: () => ({
      drawer: null,

      items: [
          { title: 'Home', icon: 'mdi-home-circle-outline',to:'/' },
          { title: 'Art', icon: 'mdi-image-multiple',to:'/art' },
          { title: 'About', icon: 'mdi-help-box',to:'/about' },
      ],

      // art:[
      //   {title:'Tink',artist:'Demonyia Lewis',img:'Tink.png'}
      // ],

    }),
  }
</script>
