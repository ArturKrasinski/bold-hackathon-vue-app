

<template>

<v-app id="inspire" dark>
    <v-navigation-drawer clipped fixed v-model="drawer" app>
        <v-list dense>
            <v-list-tile v-for="(item, i) in items" :key="i" @click="navigateTo(item.target)">
                <v-list-tile-action>
                    <v-icon v-html="item.icon"></v-icon>
                </v-list-tile-action>
                <v-list-tile-content>
                    <v-list-tile-title v-text="item.title"></v-list-tile-title>
                </v-list-tile-content>
            </v-list-tile>
        </v-list>
    </v-navigation-drawer>
    <v-toolbar app fixed clipped-left>
        <v-toolbar-side-icon @click.stop="drawer = !drawer"></v-toolbar-side-icon>
        <v-toolbar-title>Bold FE hackathon#1</v-toolbar-title>
    </v-toolbar>
    <v-content>
        <v-container fluid fill-height>
            <v-layout justify-center align-center>
                <router-view/>
            </v-layout>
        </v-container>
    </v-content>
    <v-footer app fixed>
        <span>&copy; 2018</span>
    </v-footer>
</v-app>

</template>

<script>
import Menu from '../config/menu.js'

export default {
    data () {
        return {
            clipped: false,
            drawer: false,
            fixed: false,
            items: Menu,
            miniVariant: false,
            right: true,
            rightDrawer: false,
            title: 'Vuetify.js'
        }
    },
    methods: {
        navigateTo (nav) {
            this.$router.push({
                path: nav
            })
        }
    },
    name: 'AppDark'
}
</script>
