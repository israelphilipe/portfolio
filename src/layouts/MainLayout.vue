<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated class="header items-center row justify-between">
      <div>
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
      </div>
      <q-btn
        unelevated
        class="darkModeBtn"
        @click="toggleMode"
        :label="$q.dark.mode ? 'Dark' : 'Light'"
        icon="lightbulb"
      ></q-btn>
    </q-header>
    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      :width="200"
      :breakpoint="700"
      style=""
      elevated
      class="column q-pt-xl"
    >
      <div class="q-mt-xl">
        <q-tabs vertical class="rounded-borders">
          <q-route-tab icon="home" to="/" label="home" />
          <q-route-tab icon="handyman" to="/skills" label="skills" />
          <q-route-tab icon="work" to="/projects" label="projects" />
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
import { useQuasar } from "quasar";
export default defineComponent({
  name: "MainLayout",

  components: {},

  setup() {
    const leftDrawerOpen = ref(false);
    const $q = useQuasar();
    return {
      leftDrawerOpen,
      toggleLeftDrawer() {
        leftDrawerOpen.value = !leftDrawerOpen.value;
      },
    };
  },
  created() {
    let dark =
      localStorage.getItem("darkMode") == "true" ||
      localStorage.getItem("darkMode") == null;

    this.$q.dark.set(dark);
  },
  methods: {
    toggleMode() {
      this.$q.dark.toggle();
      localStorage.setItem("darkMode", this.$q.dark.mode);
    },
  },
});
</script>
