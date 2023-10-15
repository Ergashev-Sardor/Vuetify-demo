<template>
  <v-app>
    <v-layout class="rounded rounded-md">
      <v-app-bar flat elevation="1" title="Application bar"></v-app-bar>

      <v-navigation-drawer>
        <v-list nav density="compact" color="primary">
          <v-list-item
              v-for="(item, i) in navigations"
              :key="i"
              :to="{ path: item.href }"
              color="primary"

          >
            <template v-slot:prepend>
              <v-icon :icon="item.icon"></v-icon>
            </template>

            <v-list-item-title>{{ item.text }}</v-list-item-title>
          </v-list-item>
        </v-list>

      </v-navigation-drawer>

      <v-main class="d-flex align-center justify-center" style="min-height: 300px;">
        <router-view />
      </v-main>
    </v-layout>
  </v-app>
</template>

<script>
export default {
  name: 'App',

  components: {},

  data: () => ({
    navigations: [
      { text: 'Dashboard', href: '/', icon: 'mdi-home' },
      { text: 'Buttons', href: '/buttons', icon: 'mdi-gesture-tap-button' },
      { text: 'Dialogs', href: '/dialogs', icon: 'mdi-dots-horizontal-circle-outline' },
      { text: 'Menus', href: '/menus', icon: 'mdi-menu' },
      { text: 'Carousels', href: '/carousels', icon: 'mdi-view-carousel-outline' },
      { text: 'Skeleton-loaders', href: '/Skeleton-loaders', icon: 'mdi-view-carousel-outline' },
    ]
  })
}
</script>
