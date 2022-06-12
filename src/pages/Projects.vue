<template>
  <q-page class="flex bg-dark">
    <div class="bg-dark q-pa-lg full-width text-white text-bold">
      <div>
        <div class="hello text-h2 q-my-xl">Projects that i work/worked on</div>
      </div>
      <div>
        <q-card class="bg-grey-10">
          <q-card-section class="text-h5">
            <div class="row items-center">
              <q-avatar square size="3em" class="q-mr-md">
                <img src="~/assets/med5-logo.png" />
              </q-avatar>
              MED5
            </div>
          </q-card-section>
          <q-card-section class="text-h6">
            Med5 is an ecosystem that serves to unite and facilitate medical
            assitence. It is composed of 4 main projects:
          </q-card-section>
          <q-card-section class="text-h6">
            <a href="https://med5.com.br"
              >the hub that serves as the entry for the system</a
            >
          </q-card-section>
          <q-card-section class="text-h6">
            <a href="https://app.med5.com.br"
              >the app where the customer can schedule appointments (or other
              services) and see their medical records</a
            >
          </q-card-section>
          <q-card-section class="text-h6">
            <a href="https://manager.med5.com.br"
              >the manager where the professionals and companies can manage
              their services and agendas</a
            >
          </q-card-section>
          <q-card-section class="text-h6">
            <a href="https://panel.med5.com.br"
              >And the panel that its used inside the building of the company to
              call patients in line for the appointment (or other services)
              room</a
            >
          </q-card-section>
          <q-separator class="q-mx-md" color="white"></q-separator>
          <q-card-section>
            <div class="text-h4">Role</div>
            <div class="text-h6 q-ma-md">
              Fullstack developer and tech leader of a team of 3 (myself
              included)
            </div>
          </q-card-section>
        </q-card>
      </div>
      <div class="q-my-lg">
        <q-card class="bg-grey-10">
          <q-card-section class="text-h5">
            <div class="row items-center">
              <q-avatar square size="3em" class="q-mr-md">
                <img src="~/assets/bot.png" />
              </q-avatar>
              HEADBANG
            </div>
          </q-card-section>
          <q-card-section class="text-h6">
            HeadBang is a discord bot that plays music. It was built by me when
            i was bored on lockdown. Unfortunately, some libaries needed to be
            updated and it does not work anymore
          </q-card-section>
          <q-card-section class="text-h6">
            <a href="https://github.com/israelphilipe/headBang">
              you can read the code here
            </a>
          </q-card-section>
          <q-card-section>
            <div class="text-h4">Role</div>
            <div class="text-h6 q-ma-md">Creator</div>
          </q-card-section>
        </q-card>
      </div>
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
a {
  color: white;
}
</style>
