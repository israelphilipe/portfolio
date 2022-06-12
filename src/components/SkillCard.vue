<template>
  <q-card
    class="row q-my-md items-center justify-between rounded-borders bg-grey-9"
  >
    <q-card-section class="row items-center">
      <q-avatar square size="3em">
        <img :src="skill.img" />
      </q-avatar>
      <div class="q-ml-lg">
        {{ skill.name }}
      </div>
    </q-card-section>
    <q-card-section> experience level: {{ skill.level }} </q-card-section>
  </q-card>
</template>

<script>
export default {
  props: ["skill"],
};
</script>

<style>
</style>