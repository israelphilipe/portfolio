<template>
  <q-page class="flex">
    <div class="q-pa-lg full-width text-bold">
      <div>
        <div class="hello text-h2 q-my-xl">Hello there</div>
      </div>
      <div>
        <div class="text-h4">
          <div>
            My name is Israel Philipe, i am a {{ age }} years old software developer.
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
      </div>
      <q-separator class="q-ma-md q-my-xl"></q-separator>
      <div class="text-h2 q-my-lg">Contact information</div>
      <div class="text-h5 q-my-lg">
        If you are interested you can contact me using the information bellow.
        <br />
        Email and whatsapp are my favorite options
      </div>
      <div class="text-h5">
        <div>Email : israelphilipeassuncao@gmail.com</div>
        <div>Phone : +55 84 998104581</div>
        <div>
          Github :
          <a href="https://github.com/israelphilipe">https://github.com/israelphilipe</a>
        </div>
      </div>
    </div>
  </q-page>
</template>

<script>
import { defineComponent } from "vue";

export default defineComponent({
  name: "PageIndex",
  data() {
    return {
      age: this.getAgeYear()
    }
  },
  methods: {
    getAgeYear() {
      let birthDate = new Date('03/09/1998')
      let now = new Date()
      let diff = new Date(now - birthDate)
      return Math.abs(diff.getUTCFullYear() - 1970)
    }
  }
});
</script>
<style scoped></style>
