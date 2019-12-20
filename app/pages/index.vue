<template>
  <div>
    <v-row>
      <v-col col="4">
        <v-expand-transition>
          <WelcomeCard v-if="visible" :title="'Another card'" />
        </v-expand-transition>
      </v-col>
      <v-col col="4">
        <v-scale-transition>
          <WelcomeCard v-if="visible" :title="'Another card'" />
        </v-scale-transition>
      </v-col>
      <v-col col="4">
        <v-fade-transition>
          <WelcomeCard v-if="visible" :title="'Another card'" />
        </v-fade-transition>
      </v-col>
    </v-row>

    <v-btn @click="visible = !visible">Toggle animation</v-btn>

    <div class="py-5 text-center">
      <p class="display-4">Light 96sp</p>
      <p class="display-3">Light 60sp</p>
      <p class="display-2">Regular 48sp</p>
      <p class="display-1">Regular 34sp</p>
      <p class="headline">Regular 24sp</p>
      <p class="title">Medium 20sp</p>
      <p class="subtitle-1">Regular 16sp</p>
      <p class="subtitle-2">Medium 14sp</p>
      <p class="body-1">Regular 16sp</p>
      <p class="body-2">Regular 14sp</p>
      <p class="caption">Regular 12sp</p>
      <p class="overline">Regular 10sp</p>
    </div>
  </div>
</template>

<script lang="ts">
import { Component, Vue } from "nuxt-property-decorator";
import { ExampleStore } from "~/store/example";
import { INuxtContext } from "nuxt";
import WelcomeCard from "~/components/welcome_card.vue";

@Component({
  components: {
    WelcomeCard
  }
})
export default class App extends Vue {
  visible = false;
}
</script>
