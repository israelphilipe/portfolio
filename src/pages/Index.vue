<template>
  <q-page class="flex bg-dark">
    <div class="bg-dark q-pa-lg full-width text-white text-bold">
      <q-card-section>
        <div class="hello text-h2 q-my-xl">Hello there</div>
      </q-card-section>
      <q-card-section>
        <div class="text-h4">
          <div>
            My name is Israel Philipe, i am a 24 years old software developer.
            <br />
            At the current moment i work with django using the Rest Framework on
            the backend. <br />
            However, i dabbled with laravel for a good time and have a good
            experience with it. <br />
            When it comes to the frontend side of things i mainly work with
            vueJS and quasar framework. <br />
          </div>
          <div class="q-my-md">
            Currently im working on the
            <a href="https://med5.com.br"> MED5</a> project as a fullstack
            developer and tech leader on a team of 3 (myself included).
          </div>
        </div>
        <div class="text-h4"></div>
      </q-card-section>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
});
</script>
<style scoped>
</style>
