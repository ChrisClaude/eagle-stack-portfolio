<template>
  <v-container>
    <v-row>
      <v-col sm="12" md="4" v-for="(project, x) in projects" :key="x">

        <v-card height="380px">
          <v-img
            :src="project.image"
            style="overflow: hidden; height: 150px"
            :lazy-src="`https://picsum.photos/10/6?image=${x * 5 + 10}`"
          >
            <template v-slot:placeholder>
              <v-row
                class="fill-height ma-0"
                align="center"
                justify="center"
              >
                <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
              </v-row>
            </template>
          </v-img>
          <v-card-title>
            {{project.title}}
          </v-card-title>
          <v-card-text class="card-text-height">
            {{project.text}}
          </v-card-text>
          <v-card-actions>
            <v-responsive>
              <a :href="project.link" class="mr-4" target="_blank">
                <v-btn color="primary">
                  Visit Site
                </v-btn>
              </a>
              <a :href="project.repo" target="_blank">
                <v-btn color="secondary">
                  Project Repo
                </v-btn>
              </a>
            </v-responsive>
          </v-card-actions>
        </v-card>
      </v-col>
    </v-row>

    <v-row>
      <v-col md="6" sm="8">
        <v-card>
          <v-card-text>
            <v-icon>mdi-alert</v-icon>
            This is'nt an exhaustive list, but there's more to come.
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  export default {
    data() {
      return {
        title: "C. Chris | Creations",
        projects: [
          {
            title: "Flight Booking",
            text: "Book a flight with eagle airlines",
            image: "https://res.cloudinary.com/lulendo-technologies/image/upload/v1589487936/eagle-stack/projects-img/eagle_airlines_ddw1kg.png",
            link: "https://stark-waters-39409.herokuapp.com/",
            repo: "https://github.com/ChClaude/eagle-airlines"
          },{
            title: "Movie Streamer",
            text: "Find and stream movie, built with React JS",
            image: "https://res.cloudinary.com/lulendo-technologies/image/upload/v1589487966/eagle-stack/projects-img/hubstack_stream_vr9z6v.png",
            link: "https://claude-ns.netlify.app",
            repo: "https://github.com/ChClaude/hubstuck-stram"
          },
          {
            title: "Github Finder",
            text: "Single Page github finder app, interact with the github API and find almost anything around github users",
            image: "https://res.cloudinary.com/lulendo-technologies/image/upload/v1589487936/eagle-stack/projects-img/github_finder_jqmdop.png",
            link: "https://githubfinder-c.netlify.app",
            repo: "https://github.com/ChClaude/github-finder-m"
          },
          {
            title: "EagleStack",
            text: "This is my portfolio site - I named it Eagle Stack",
            image: "https://res.cloudinary.com/lulendo-technologies/image/upload/v1589487964/eagle-stack/projects-img/eagle_stack_nt38nq.png",
            link: "https://cchris.netlify.app",
            repo: "https://github.com/ChClaude/eagle-stack-portfolio"
          },
          {
            title: "Joky Jokes",
            text: "Site for jokes, this is a site I built while getting to know the Nuxt JS framework",
            image: "https://res.cloudinary.com/lulendo-technologies/image/upload/v1589487936/eagle-stack/projects-img/dad_jokes_dxqa66.png",
            link: "https://nuxt-jokes.netlify.app",
            repo: "https://github.com/ChClaude/nuxtjs-dad-jokes"
          },
          {
            title: "Portfolio Site",
            text: "This was my previous portfolio site",
            image: "https://res.cloudinary.com/lulendo-technologies/image/upload/v1589487974/eagle-stack/projects-img/lulendo_site_qcjelf.png",
            link: "https://lulendo-chclaude.netlify.app",
            repo: "https://github.com/ChClaude/lulendo-claude-portfolio"
          },
          {
            title: "Phono Site",
            text: "This is a static site, just for display, phono site",
            image: "https://res.cloudinary.com/lulendo-technologies/image/upload/v1589487943/eagle-stack/projects-img/phono_site_cax4zv.png",
            link: "https://claude-phono-website.netlify.app",
            repo: "https://github.com/ChClaude/phono-website"
          }
        ]
      }
    },
    methods: {},
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
  a {
    text-decoration: none;
  }

  .card-text-height {
    height: 80px;
  }
</style>
