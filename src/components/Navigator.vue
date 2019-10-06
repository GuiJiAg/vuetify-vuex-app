<template>
    <span>
        <v-navigation-drawer
          app 
          bottom 
          v-model="drawer" 
          color="amber lighten-1" 
          dark 
          disable-resize-watcher>
            <v-icon medium color="white" class="margin-button" @click="drawer = !drawer">clear</v-icon>
            <v-list>
                <template v-for="(item, index) in items">
                    <v-list-item :key="index">
                        <v-list-item-content>
                            {{ item.title }}
                        </v-list-item-content>
                    </v-list-item>
                    <v-divider :key="`divider-${index}`"></v-divider>
                </template>
            </v-list>
        </v-navigation-drawer>
        <v-app-bar color="amber darken-4" dark>
            <v-app-bar-nav-icon class="hidden-md-and-up" @click="drawer = !drawer"></v-app-bar-nav-icon>
            <v-spacer class="hidden-md-and-up"></v-spacer>
            <v-toolbar-title>{{ appTitle }}</v-toolbar-title>
            <v-btn text class="hidden-sm-and-down margin-button">Menu</v-btn>
            <v-spacer class="hidden-sm-and-down"></v-spacer>
            <v-btn text class="hidden-sm-and-down margin-button">Sign In</v-btn>
            <v-btn color="amber lighten-3" class="hidden-sm-and-down margin-button black--text">Join</v-btn>
        </v-app-bar>
    </span> 
</template>

<script>
export default {
    name: 'Navigator',
    data() {
        return {
            appTitle: 'Vue App',
            drawer: false,
            items: [
                { title: 'Menu' },
                { title: 'Sign In' },
                { title: 'Join'}
            ]
        };
    }
}
</script>

<style scoped>
    .margin-button {
        margin: 10px;
    }
</style>