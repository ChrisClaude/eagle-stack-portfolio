<template>
  <v-container class="fill-height" fluid>
    <v-row>
      <v-col
        cols="8"
      >
        <v-hover
          v-slot:default="{ hover }"
          open-delay="200"
        >
          <v-card
            :elevation="hover ? 16 : 2"
            min-height="350"
          >
            <v-card-title>
              About Chris
            </v-card-title>
            <v-card-text class="subtitle-1">
              <p>I am a passionate software developer. I love solving problems and helping business grow. I am constantly looking for perfection.</p>
              <p>As of the time I am writing this, I am primarily working on personal open source projects and studying for a BTech in Software development;
                you can see my latest activities <nuxt-link to="/#github_activities">here</nuxt-link></p>
              <p>You have a great idea? a business in mind? want a developer or a collaborator? email me <a
                href="mailto:christ.tchambila@gmail.com">christ.tchambila@gmail.com</a> or contact me <nuxt-link to="contact">here</nuxt-link> I'll get back to you.</p>
            </v-card-text>
          </v-card>
        </v-hover>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data() {
      return {
        title: "C. Chris | About"
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

<style scoped>

</style>
