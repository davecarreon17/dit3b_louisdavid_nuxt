<template>
  <div>
    <v-app>

    <!-- Navigation -->
       <v-navigation-drawer
        v-model = "drawer"
      >
        <v-list>
          <v-list-item
            prepend-avatar="https://randomuser.me/api/portraits/women/85.jpg"
            subtitle="DIT - 3B"
            title="Louis David S. Carreon"
          ></v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item to="/dashboard" prepend-icon="mdi-folder" title="Dashboards" value="myfiles"></v-list-item>
          <v-list-item to="/inventory" prepend-icon="mdi-account-multiple" title="Inventory" value="shared"></v-list-item>
          <v-list-item to="/category" prepend-icon="mdi-star" title="Category" value="Category"></v-list-item>
          <v-list-item to="/users" prepend-icon="mdi mdi-account" title="Users" value="Category"></v-list-item>
        </v-list>
      </v-navigation-drawer>


        <!-- Navigation -->



    <!-- AppBar -->
        <v-app-bar :elevation="2">
  <template v-slot:prepend>
    <v-app-bar-nav-icon @click.stop="drawer =! drawer"></v-app-bar-nav-icon>
  </template>

  <v-app-bar-title>Application Bar</v-app-bar-title>
</v-app-bar>



        <!-- AppBar -->
      <v-main>
        <v-container>
            <slot />
        </v-container>
      </v-main>
    </v-app>
  </div>
</template>

<script setup>
const drawer= ref(true)

</script>

<style>

</style>