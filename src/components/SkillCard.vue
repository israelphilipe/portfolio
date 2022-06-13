<template>
  <q-card class="row q-my-md items-center justify-between rounded-borders">
    <q-card-section class="row items-center">
      <q-avatar square class="q-mr-md">
        <img :src="skill.img" />
      </q-avatar>
      <div class="text-h6">
        {{ skill.name }}
      </div>
    </q-card-section>
    <q-badge
      class="text-h6 text-bold q-px-lg"
      style="border-radius: 15px"
      floating
      :color="color"
    >
      {{ skill.level }}
    </q-badge>
  </q-card>
</template>

<script>
export default {
  props: ["skill"],
  computed: {
    color() {
      let color = "positive";
      if (this.skill.level == "medium") {
        color = "warning";
      }
      return color;
    },
  },
};
</script>

<style>
</style>