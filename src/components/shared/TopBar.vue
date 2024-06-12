<template>
    <v-toolbar
        image="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
        prominent
    >
        <v-app-bar-nav-icon></v-app-bar-nav-icon>

        <v-toolbar-title>Wovenware</v-toolbar-title>

        <v-spacer></v-spacer>
        <v-btn icon @click="toggleTheme">
            <v-icon>mdi-lightbulb-on</v-icon>
        </v-btn>
        <v-btn icon>
            <v-icon>mdi-export</v-icon>
        </v-btn>
    </v-toolbar>
</template>

<script setup>
import { useTheme } from "vuetify";

const theme = useTheme();
function toggleTheme() {
    theme.global.name.value = theme.global.current.value.dark
        ? "light"
        : "dark";
}
</script>
