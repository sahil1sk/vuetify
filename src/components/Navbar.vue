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

        <div class="text-center">
            <v-menu offset-y>
            <template v-slot:activator="{ on, attrs }">
                <v-btn
                depressed
                v-bind="attrs"
                v-on="on"
                class="grey--text"
                >
                <v-icon left>expand_more</v-icon>
                <span>Menu</span>
                </v-btn>
            </template>
            <v-list>
                <v-list-item
                v-for="(link, index) in links"
                :key="index"
                router :to="link.route"
                >
                <v-list-item-title>{{ link.text }}</v-list-item-title>
                </v-list-item>
            </v-list>
            </v-menu>
        </div>

        <v-btn depressed class="transparent text--grey font-weight-light">
            <span>Sign Out</span>
            <v-icon right>exit_to_app</v-icon>
        </v-btn>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" app class="primary">
        <div class="text-center">
            <v-col class="mt-5">
                <v-avatar size="100" class="mt-5">
                    <img src="/avatarImg.png" alt="avatar">
                </v-avatar>
                <p class="white--text subheading mt-1">
                    The Net Ninja
                </p>
            </v-col>
            <v-col class="mt-4 mb-3">
                <Popup />
            </v-col>
        </div>
        <v-list>
            <v-list-item v-for="(link, i) in links" :key="i" router :to="link.route">
                <v-list-item-action>
                    <v-icon class="white--text">
                        {{ link.icon }}
                    </v-icon>
                </v-list-item-action>
                <v-list-item-content>
                    <v-list-item-title class="white--text">
                        {{ link.text }}
                    </v-list-item-title>
                </v-list-item-content>
            </v-list-item>
        </v-list>
    </v-navigation-drawer>

  </nav>
</template>

<script>
import Popup from './Popup.vue'

export default {
    components: { Popup },
    data() {
        return {
            drawer: false,
            links: [
                { icon: 'dashboard', text: 'Dashboard', route: '/' },
                { icon: 'folder', text: 'My Projects', route: '/projects' },
                { icon: 'person', text: 'Team', route: '/team' },
            ]
        }
    }
}
</script>
