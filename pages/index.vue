<template>
  <v-layout
    column
    justify-center
    align-center
  >
    <!--  Caroussel  -->
    <v-carousel
      cycle
      height="500"
      hide-delimiter-background
      show-arrows-on-hover
    >
      <!--   First Slide   -->
      <v-carousel-item>
        <v-row
          class="fill-height"
        >
          <v-img
            src="/city_entreprise.jpg"
            lazy-src="/city_entreprise.jpg"
            class="d-flex justify-end align-center">
                  <div class="display-3 white--text d-flex justify-center pl-5">Welcome <br/>to Chris Software development World</div>
          </v-img>
          <template v-slot:placeholder>
            <v-row
              class="fill-height ma-0"
              align="center"
              justify="center"
            >
              <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
            </v-row>
          </template>
        </v-row>
      </v-carousel-item>
      <!--   Second First   -->
      <v-carousel-item>
        <v-row
          class="fill-height"
        >
          <v-img
            src="software_dev.jpg"
            lazy-src="/city_entreprise.jpg"
            class="d-flex justify-end align-center">
            <div class="white--text pr-6" style="display: grid; grid-template-columns: auto;">
              <blockquote class="blockquote" style="text-align: right;">
                Want to hire me or collaborate?
              </blockquote>
              <div>
                <v-btn to="/contact" class="primary" style="float: right;">
                  Contact me
                </v-btn>
              </div>
            </div>
          </v-img>
          <template v-slot:placeholder>
            <v-row
              class="fill-height ma-0"
              align="center"
              justify="center"
            >
              <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
            </v-row>
          </template>
        </v-row>
      </v-carousel-item>
      <!--   Third First   -->
      <v-carousel-item>
        <v-row
          class="fill-height flex-column"
          align="center"
          justify="center"
        >
          <v-img
            src="/silver-and-black-laptop-computer.jpg"
            lazy-src="/city_entreprise.jpg"
            class="d-flex align-center">
            <v-container class="white--text">
              <v-row class="pl-6" justify="center">
                <v-col cols="4">
                  <v-row class="display-1 white--text">
                    Be amazed by my work
                  </v-row>
                  <v-row class="mt-3">
                    <v-btn class="primary" to="/creations">Explore</v-btn>
                  </v-row>
                </v-col>
              </v-row>
            </v-container>
          </v-img>
          <template v-slot:placeholder>
            <v-row
              class="fill-height ma-0"
              align="center"
              justify="center"
            >
              <v-progress-circular indeterminate color="grey lighten-5"></v-progress-circular>
            </v-row>
          </template>
        </v-row>
      </v-carousel-item>
    </v-carousel>

    <!-- Services and Stacks -->
    <v-container>
      <!--  Services offered  -->
      <v-row>
        <v-col cols="12" height="270">
          <span>Services</span>
          <v-icon>
            mdi-chevron-right
          </v-icon>
        </v-col>
        <v-col v-for="service in services" sm="12" md="4" :key="service.id">
          <v-card class="card-services-height">
            <v-img
              :src="service.image"
              class="white--text card-services-img"
              lazy-src="https://picsum.photos/10/6?image=10"
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
              {{service.title}}
            </v-card-title>
            <v-card-text class="card-services-text">
              <div>
                {{service.text}}
              </div>
            </v-card-text>
            <v-card-actions>
              <v-btn to="/contact" color="primary">
                Start
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>

      </v-row>

      <!--   Stack used   -->
      <v-container>
        <v-row class="mb-2">
          <v-col cols="12">
            <div class="font-34"><b>Technologies</b> at your service</div>
          </v-col>
          <div class="bar"></div>
        </v-row>

        <v-row>
          <v-col v-for="stack in stacks" sm="6" md="3" :key="stack.id">
            <v-card class="card-stack-height">
              <v-container class="card-stack-img">
                <v-img :src="stack.image"></v-img>
              </v-container>
              <v-card-title class="pb-0">{{stack.title}}</v-card-title>
              <v-card-text class="card-text">
                <div>{{stack.text}}</div>
              </v-card-text>
              <v-card-actions>
                <v-btn
                  to="/creations"
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
    </v-container>

    <!--  Social Media Section  -->
    <v-container>
      <v-row class="mb-2">
        <v-col cols="12">
          <h2>Social Media</h2>
        </v-col>
      </v-row>
      <v-row class="social-med-row">
        <!--  LinkedIn  -->
        <v-col sm="6" md="3" class="mt-3 mb-2">
          <v-card>
            <v-card-title class="card-tile-height">
              <a href="https://www.linkedin.com/in/claude-de-tchambila-a720ba143/" target="_blank">
                <v-card color="#0077B5" class="icon-pos">
                  <v-card-title class="pa-6">
                    <v-icon color="#fff" x-large>mdi-linkedin</v-icon>
                  </v-card-title>
                </v-card>
              </a>
            </v-card-title>
            <v-card-text>
              <v-divider class="my-3"></v-divider>
              <v-icon>mdi-transfer-up</v-icon>
              Contact me on LinkedIn
            </v-card-text>
          </v-card>
        </v-col>
        <!--  Github  -->
        <v-col sm="6" md="3" class="mt-3 mb-2">
          <v-card>
            <v-card-title class="card-tile-height">
              <a href="https://github.com/ChCLaude" target="_blank">
                <v-card color="#24292E" class="icon-pos">
                  <v-card-title class="pa-6">
                    <v-icon color="#fff" x-large>mdi-github</v-icon>
                  </v-card-title>
                </v-card>
              </a>
            </v-card-title>
            <v-card-text>
              <v-divider class="my-3"></v-divider>
              <v-icon>mdi-transfer-up</v-icon>
              Follow me on Github
            </v-card-text>
          </v-card>
        </v-col>
        <!--  Twitter  -->
        <v-col sm="6" md="3" class="mt-3 mb-2">
          <v-card>
            <v-card-title class="card-tile-height">
              <a href="https://twitter.com/ClaudeChrist_DT" target="_blank">
                <v-card color="#00cae3" class="icon-pos">
                  <v-card-title class="pa-6">
                    <v-icon color="#fff" x-large>mdi-twitter</v-icon>
                  </v-card-title>
                </v-card>
              </a>
            </v-card-title>
            <v-card-text>
              <v-divider class="my-3"></v-divider>
              <v-icon>mdi-transfer-up</v-icon>
              Follow me on Twitter
            </v-card-text>
          </v-card>
        </v-col>
        <!--  Instagram  -->
        <v-col sm="6" md="3" class="mt-3 mb-2">
          <v-card>
            <v-card-title class="card-tile-height">
              <a href="https://www.instagram.com/christ_tchambila/" target="_blank">
                <v-card color="#EC6343" class="icon-pos">
                  <v-card-title class="pa-6">
                    <v-icon color="#fff" x-large>mdi-instagram</v-icon>
                  </v-card-title>
                </v-card>
              </a>
            </v-card-title>
            <v-card-text>
              <v-divider class="my-3"></v-divider>
              <v-icon>mdi-transfer-up</v-icon>
              Follow me on Instagram
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

    <!--    Latest Development Activities on Github  -->
    <v-container>
      <v-row>
        <v-col cols="12">
          <h2 id="github_activities">Latest Github Activities</h2>
        </v-col>
        <v-col sm="12" md="8">
          <v-card>
            <v-card-title>
              <v-avatar color="orange" size="62">
                <v-img :src="githubData.avatar_url"></v-img>
              </v-avatar>
              <div class="ml-4 subtitle-1">
                <div class="mb-1">Username:
                  <v-chip color="primary">
                    <v-icon class="mr-1">mdi-account-outline</v-icon>
                    {{githubData.login}}
                  </v-chip>
                </div>
                <div class="mb-1">Location:
                  <v-chip color="info">
                    <v-icon class="mr-1">mdi-map-marker</v-icon>
                    {{githubData.location}}
                  </v-chip>
                </div>
                <div class="mb-1">Hireable:
                  <v-chip color="success">
                    <v-icon class="mr-1">{{githubData.hireable? "mdi-account-check" : "mdi-account-off"}}</v-icon>
                    {{githubData.hireable? "Yes" : "No"}}
                  </v-chip>
                </div>
              </div>
            </v-card-title>
            <v-card-text>
              <v-row v-if="githubEventData.length > 0">
                <v-col cols="12" v-for="x in 3" :key="x">
                  <div>
                    Type: {{githubEventData[x-1].type}}
                  </div>
                  <div>
                    Actor: {{githubEventData[x-1].actor.login}}
                  </div>
                  <div>
                    Url: <a :href="githubEventData[x-1].repo.url">{{githubEventData[x].repo.name}}</a>
                  </div>
                  <div v-if="githubEventData[x-1].payload.commits">
                    Commit message: {{githubEventData[x-1].payload.commits[0].message}}
                  </div>
                  <div>
                    Created at: {{new Date(githubEventData[x].created_at)}}
                  </div>
                  <v-divider class="mt-1"></v-divider>
                </v-col>
                <v-col sm="12" md="6">
                  <v-icon>mdi-clock</v-icon>
                  Tracked From Github
                </v-col>
              </v-row>
              <div v-show="githubEventData.length === 0">
                No activities recorded
              </div>
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  </v-layout>
</template>

<script>
  import axios from "axios";

  export default {
    components: {},
    data() {
      return {
        title: "C. Chris | Portfolio",
        githubData: {},
        githubEventData: [],
        services: [
          {
            id: "service1",
            image: "/webdevelopment.jpg",
            title: "Web development",
            text: "Be amazed with what we have to offer. End to end solution, " +
              "we take your business from an idea to a real app in production.",
            link: ""
          },
          {
            id: "service2",
            image: "/desktopdev.jpg",
            title: "Desktop development",
            text: "We build the desktop apps your business needs.",
            link: ""
          },
          {
            id: "service3",
            image: "/white-iphone-xr.jpg",
            title: "iOS development",
            text: "Robust and scalable.We prototype beforehand, you either like it or you don't owe us.",
            link: ""
          },
          {
            id: "service4",
            image: "/android-android-phone-cel.jpg",
            title: "Android development",
            text: "We build native android applications for mobiles Build your android solution with us. " +
              "We prototype, you either like or you don't pay.",
            link: ""
          }
        ],
        stacks: [
          {
            id: "stack_1",
            image: "/laravel-2.svg",
            title: "Laravel",
            text: "Thanks to this wonderful web framework we can build robust and scalable web apps",
            "link": ""
          },
          {
            id: "stack_2",
            image: "/vue-js-1.svg",
            title: "Vue JS",
            text: "We build the UI that makes your business stand out",
            "link": ""
          },
          {
            id: "stack_3",
            image: "/python-logo.svg",
            title: "Python",
            text: "Artificial Intelligence and Machine Learning capabilities plugged into your web apps",
            "link": ""
          },
          {
            id: "stack_4",
            image: "/c--4.svg",
            title: "C#",
            text: "Web, desktop, mobile apps and others built with Microsoft Technologies.",
            "link": ""
          }
        ]
      }
    },
    async created() {
      const res = await axios.get(`https://api.github.com/users/chclaude?client_id=${process.env.GITHUB_CLIENT_ID}
      &client_secret=${process.env.GITHUB_CLIENT_SECRET}`)
        .catch(error => console.log(error));

      const resEvent = await axios.get(`https://api.github.com/users/ChClaude/events?client_id=${process.env.GITHUB_CLIENT_ID}
      &client_secret=${process.env.GITHUB_CLIENT_SECRET}`)
        .catch(error => console.log(error));

      if (res !== undefined && resEvent !== undefined) {
        this.githubData = res.data;
        this.githubEventData = resEvent.data;
      }

      // console.log("Login");
      // console.log(process.env.githubClientId);
      // console.log(process.env.githubClientSecret);
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
  .card-services-height {
    height: 500px;
  }

  .card-services-img {
    height: 270px;
  }

  .card-services-text {
    height: 100px;
    display: flex;
    align-items: center;
  }

  .icon-pos {
    position: relative;
    top: -37px;
  }

  .card-stack-img {
    height: 255px;
    overflow: hidden;
  }

  .card-text {
    display: flex;
    align-items: center;
    height: 100px;
  }

  .card-tile-height {
    max-height: 70px;
  }

  .card-tile-height a {
    text-decoration: none;
  }

  .card-stack-height {
    height: 460px;
  }

  .font-34 {
    font-size: 30px;
    font-weight: 400;
  }

  .bar {
    position: relative;
    left: 12px;
    top: -4px;
    width: 100px;
    height: 2px;
    border-radius: 1px;
    background-color: #fc4364;
  }

  @media only screen and (max-width: 600px) {
    .social-med-row {
      display: grid;
      grid-template-columns: auto auto;
    }

    .card-stack-img {
      height: 285px;
    }

    .card-stack-height {
      height: 490px;
    }

    .icon-pos {
      top: -22px;
    }
  }
</style>
