<template>
  <v-card class="overflow-hidden">
    <v-app-bar
      absolute
      color="#fcb69f"
      dark
      shrink-on-scroll
      src="https://cdn.pixabay.com/photo/2019/11/04/16/56/donations-keeps-me-going-4601584_640.jpg"
      scroll-target="#scrolling-techniques-2"
    >
      <template v-slot:img="{ props }">
        <v-img v-bind="props"> </v-img>
      </template>

      <v-app-bar-nav-icon @click.stop="drawer = !drawer"> </v-app-bar-nav-icon>

      <v-toolbar-title>Book Creatives</v-toolbar-title>

      <v-spacer></v-spacer>

      <v-btn icon>
        <v-icon>mdi-magnify</v-icon>
      </v-btn>
    </v-app-bar>

    <v-navigation-drawer
      class="bg-gradient-to-tr from-pink-120 via-blue-300 to-green-500"
      v-model="drawer"
      absolute
      leftDrawerOpen
      temporary
      src="@/assets/pexels-wendy-wei-1190297.jpg"
      gradient="bg-gradient-to-tr from-pink-120 via-blue-300 to-green-500"
    >
      <v-list nav dense>
        <v-list-item-group
          v-model="group"
          active-class="deep-white--text text--accent-4"
        >
          <v-list-item class="text-white">
            <v-list-item-title class="text-white"
              >All Creatives</v-list-item-title
            >
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="text-white">Amapiano</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="text-white">Hiphop</v-list-item-title>
          </v-list-item>

          <v-list-item>
            <v-list-item-title class="text-white">Jazz</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title class="text-white">Maskandi</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title class="text-white">Gospel</v-list-item-title>
          </v-list-item>
          <v-list-item>
            <v-list-item-title class="text-white">Afrobeats</v-list-item-title>
          </v-list-item>
        </v-list-item-group>
      </v-list>
    </v-navigation-drawer>
    <v-spacer></v-spacer>

    <v-btn icon>
      <v-icon>mdi-magnify</v-icon>
    </v-btn>

    <v-sheet
      id="scrolling-techniques-2"
      class="overflow-y-auto"
      max-height="600"
    >
      <v-container style="height: 1000px"></v-container>
    </v-sheet>
  </v-card>
</template>

<script>
export default {
  name: "App",

  data: () => ({
    drawer: null,
  }),
};
</script>
