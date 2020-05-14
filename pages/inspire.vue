<template>
  <v-layout>
    <v-flex class="text-center">
      <img
        src="https://res.cloudinary.com/lulendo-technologies/image/upload/v1589488298/eagle-stack/vuetify-logo_n6o1du.svg"
        alt="Vuetify.js"
        class="mb-5"
      >
      <blockquote class="blockquote">
        &#8220;First, solve the problem. Then, write the code.&#8221;
        <footer>
          <small>
            <em>&mdash;John Johnson</em>
          </small>
        </footer>
      </blockquote>
    </v-flex>
  </v-layout>
</template>

<script>
  export default {
    data () {
      return {
        title: "C. Chris | Skills"
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
