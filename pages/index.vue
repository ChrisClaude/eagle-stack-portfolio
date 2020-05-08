<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <v-container>
      <h1 class="text-center">Welcome</h1>
      <v-row>
        <v-col cols="3">
          <v-card class="height-430">
            <v-container>
              <v-img src="laravel-2.svg"></v-img>
            </v-container>
            <v-card-subtitle class="pb-0">Laravel</v-card-subtitle>
            <v-card-text>
              <div>Web apps, desktop apps and others built with Microsoft Technologies</div>
            </v-card-text>
            <v-card-actions>
              <v-btn
                color="primary"
                text
              >
                Explore
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="3">
          <v-card class="height-430">
            <v-container>
              <v-img src="vue-js-1.svg"></v-img>
            </v-container>
            <v-card-subtitle class="pb-0">Vue JS</v-card-subtitle>
            <v-card-text>
              <div>We build the UI that makes your business stand out</div>
            </v-card-text>
            <v-card-actions>
              <v-btn
                color="primary"
                text
              >
                Explore
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="3">
          <v-card class="height-430">
            <v-container>
              <v-img src="python-logo.svg"></v-img>
            </v-container>
            <v-card-subtitle class="pb-0">Python</v-card-subtitle>
            <v-card-text>
              <div>Web apps, desktop apps and others built with Microsoft Technologies</div>
            </v-card-text>
            <v-card-actions>
              <v-btn
                color="primary"
                text
              >
                Explore
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="3">
          <v-card class="height-430">
            <v-container>
              <v-img src="/c--4.svg"></v-img>
            </v-container>
            <v-card-subtitle class="pb-0">C#</v-card-subtitle>
            <v-card-text>
              <div>Web apps, desktop apps and others built with Microsoft Technologies</div>
            </v-card-text>
            <v-card-actions>
              <v-btn
                color="primary"
                text
              >
                Explore
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>

  export default {
    components: {},
    data() {
      return {
        title: "C. Chris | Portfolio",
      }
    },
    head() {
      return {
        title: this.title,
        meta: [
          {hid: 'description', name: 'description', content: 'Claude Christ De-Tchambila Portfolio'}
        ]
      }
    }
  }
</script>
<style>
  .bg {
    background-image: url("/silver-and-black-laptop-computer.jpg");
    background-size: cover;
  }

  .height-430 {
    height: 430px;
  }
</style>
