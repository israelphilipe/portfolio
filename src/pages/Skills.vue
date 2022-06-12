<template>
  <q-page class="flex bg-dark">
    <div class="bg-dark q-pa-lg full-width text-white text-bold">
      <div class="q-my-xl">
        <div class="hello text-h2">Skills</div>
        <div class="text-h6 q-ml-sm">
          So... here are my skills (programming languages, frameworks and
          tecnologies)
        </div>
      </div>
      <div>
        <div class="text-h5 q-ml-md">
          Programming laguanges
          <div class="row full-width">
            <div
              class="col-md-5 col-12 q-mr-md"
              v-for="(language, index) in languages"
              :key="index"
            >
              <SkillCard :skill="language" />
            </div>
          </div>
        </div>
      </div>
      <div>
        <div class="text-h5 q-ml-md">
          Backend frameworks
          <div class="row full-width">
            <div
              class="col-md-5 col-12 q-mr-md"
              v-for="(framework, index) in backendFrameworks"
              :key="index"
            >
              <SkillCard :skill="framework" />
            </div>
          </div>
        </div>
      </div>
      <div>
        <div class="text-h5 q-ml-md">
          Frontend frameworks
          <div class="row full-width">
            <div
              class="col-md-5 col-12 q-mr-md"
              v-for="(framework, index) in frontendFrameorks"
              :key="index"
            >
              <SkillCard :skill="framework" />
            </div>
          </div>
        </div>
      </div>
      <div>
        <div class="text-h5 q-ml-md">
          Other skills
          <div class="row full-width">
            <div
              class="col-md-5 col-12 q-mr-md"
              v-for="(skill, index) in extra"
              :key="index"
            >
              <SkillCard :skill="skill" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </q-page>
</template>
<script>
import { defineComponent } from "vue";
import SkillCard from "components/SkillCard.vue";
export default defineComponent({
  name: "PageIndex",
  components: {
    SkillCard,
  },
  data() {
    return {
      languages: [
        {
          name: "Python",
          img: require("assets/python.png"),
          level: "good",
        },
        {
          name: "Php",
          img: require("assets/php.png"),
          level: "good",
        },
        {
          name: "Javascript",
          img: require("assets/javascript.png"),
          level: "good",
        },
      ],
      backendFrameworks: [
        {
          name: "Django Rest",
          img: require("assets/djangorest.png"),
          level: "good",
        },

        {
          name: "Laravel",
          img: require("assets/laravel.png"),
          level: "good",
        },
      ],
      frontendFrameorks: [
        {
          name: "Vue",
          img: require("assets/vue.png"),
          level: "good",
        },
        {
          name: "Quasar",
          img: require("assets/quasar.svg"),
          level: "good",
        },
      ],
      extra: [
        {
          name: "Juno",
          img: require("assets/juno.png"),
          level: "medium",
        },
        {
          name: "Arduino",
          img: require("assets/arduino.png"),
          level: "medium",
        },
        {
          name: "Scrum",
          img: require("assets/scrum.svg"),
          level: "good",
        },
      ],
    };
  },
});
</script>
<style scoped>
</style>
