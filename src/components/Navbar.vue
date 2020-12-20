<template>
  <nav>
    <!-- flat make it transparent -->
    <v-app-bar app flat>
        <v-app-bar-nav-icon class="grey--text" @click="drawer = !drawer"></v-app-bar-nav-icon>
        <v-toolbar-title class="text-uppercase grey--text">
            <span class="font-weight-light">Todo</span>
            <span>Ninja</span>
        </v-toolbar-title>
        <v-spacer></v-spacer>
        <v-btn depressed class="transparent text-grey font-weight-light">
            <span>Sign Out</span>
            <v-icon right>exit_to_app</v-icon>
        </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app class="indigo">
        <p>test</p>
    </v-navigation-drawer>

  </nav>
</template>

<script>
export default {
    data() {
        return {
            drawer: false
        }
    }
}
</script>
