<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="bg-dark text-red">
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="toggleLeftDrawer"
        />

        <q-toolbar-title> Israel </q-toolbar-title>
      </q-toolbar>
    </q-header>
    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      :width="200"
      :breakpoint="700"
      style=""
      elevated
      class="bg-dark text-red column q-pt-xl"
    >
      <div class="q-mt-xl">
        <q-tabs vertical class="rounded-borders">
          <q-route-tab icon="home" to="/" label="home" />
          <q-route-tab icon="handyman" to="/skills" label="skills" />
          <q-route-tab icon="work" to="/projects" label="projects" />
          <q-route-tab icon="person" to="/me" label="about me" />
        </q-tabs>
      </div>
    </q-drawer>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import { defineComponent, ref } from "vue";

export default defineComponent({
  name: "MainLayout",

  components: {},

  setup() {
    const leftDrawerOpen = ref(false);

    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
});
</script>
