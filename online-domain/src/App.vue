<script setup></script>

<template>
  <v-app>
    <v-app-bar :elevation="2" density="compact"
      color="primary">
        <template v-slot:prepend>
          <v-app-bar-nav-icon></v-app-bar-nav-icon>
        </template>
        <v-app-bar-title>Obed Oyandut</v-app-bar-title>
        <template v-slot:append>
          <v-btn icon="mdi-dots-vertical"></v-btn>
        </template>
    </v-app-bar>
    <v-main>
      <v-container fluid>
        <v-row>
          <v-col cols="3" class="firstcolumn">
            <v-navigation-drawer theme="grey" permanent rail style="width: 20vw">
              <v-list>
                <v-list-item prepend-avatar="pic/cv.jpg">
                  Personal Information
                </v-list-item>
              </v-list>
            </v-navigation-drawer>
          </v-col>
          <v-col cols="6" class="middlecolumn"></v-col>
          <v-col cols="3" class="thirdcolumn"></v-col>
        </v-row>
    </v-container>
    </v-main>
  </v-app>
</template>

<style scoped>
  .firstcolumn {
    /* width: 25vw; */
    height: 50vh;
    border: 1px solid white;
  }
  .middlecolumn {
    /* width: 50vw; */
    height: 100vh;
    border: 1px solid blue;
    border-radius: 4%;
  }
  .thirdcolumn {
    /* width: 25vw; */
    height: 75vh;
    border: 1px solid white;
  }
</style>
