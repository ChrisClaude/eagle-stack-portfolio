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
          align="center"
          justify="center"
        >
          <v-img
            src="/city_entreprise.jpg"
            lazy-src="/city_entreprise.jpg"
            class="d-flex justify-end align-center">
            <v-container class="white--text" style="position: relative; top: -110px;">
              <v-row class="pl-6">
                <v-col cols="12 ">
                  <div class="display-3 white--text">Welcome <br/>to Chris Software development World</div>
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

      <!--   Second First   -->
      <v-carousel-item>
        <v-row
          class="fill-height pr-12"
        >
          <v-img
            src="/software_dev.jpg"
            lazy-src="/city_entreprise.jpg"
            class="d-flex justify-end align-center">
            <v-container class="white--text pr-8 rt-80">
              <v-row justify="end" class="pr-10">
                <v-col cols="12 text-right">
                  <blockquote class="blockquote">
                    Want to hire me or collaborate?
                  </blockquote>
                </v-col>
                <v-col cols="2" style="position: relative; top: -20px;">
                  <v-btn class="primary">
                    Contact me
                  </v-btn>
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
                    Be amazed my work
                  </v-row>
                  <v-row class="mt-3">
                    <v-btn class="primary">Explore</v-btn>
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

    <v-container>
      <v-row>
        <v-col cols="12" height="270">
          <span>Services</span>
          <v-icon>
            mdi-chevron-right
          </v-icon>
        </v-col>
        <v-col cols="4">
          <v-card>
            <v-img src="/webdevelopment.jpg" class="white--text" height="270px">
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
            <v-card-text>
              <div>
                <b>Web Development</b>, be amazed with what we have to offer.
                End to end solution, we take your business from an idea to a real app in production.
              </div>
            </v-card-text>
            <v-card-actions>
              <v-btn>
                Contact
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card>
            <v-img
              src="/desktopdev.jpg"
              lazy-src="https://i.picsum.photos/id/0/200/200.jpg"
              class="white--text" height="270px">
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
            <v-card-text>
              <b>Desktop development</b>, we build the desktop apps your business needs.
            </v-card-text>
            <v-card-actions>
              <v-btn>
                Contact
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card>
            <v-container>
              <v-img
                src="/apple-ios.svg"
                lazy-src="https://i.picsum.photos/id/0/200/200.jpg"
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
            </v-container>
            <v-card-text>
              <div><b>iOS development</b>, robust and scalable.</div>
              <div>We prototype beforehand, you either like it or you don't owe us.</div>
            </v-card-text>
            <v-card-actions>
              <v-btn>
                Contact
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
        <v-col cols="4">
          <v-card>
            <v-container>
              <v-img
                src="/android-5.svg"
                lazy-src="https://i.picsum.photos/id/0/200/200.jpg"
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
            </v-container>
            <v-card-text>
              <div>We build <b>native android applications</b> for mobiles</div>
              <div>Build your android solution with us.</div>
              <div>We prototype, you either like or you don't pay.</div>
            </v-card-text>
            <v-card-actions>
              <v-btn>
                Contact
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>


      <v-container>
        <v-row class="mb-2">
          <v-col cols="12">
            <div class="font-34"><b>Technologies</b> at your service</div>
          </v-col>
          <div class="bar"></div>
        </v-row>

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
              <v-container style="height: 265px;">
                <v-img src="vue-js-1.svg" class="vue-img"></v-img>
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
    </v-container>

  <!--  Social Media Section  -->
    <v-container>
      <v-row class="mb-3">
        <v-col cols="12">
          <h2>Social Media</h2>
        </v-col>
      </v-row>
      <v-row>
      <!--  LinkedIn  -->
        <v-col cols="3">
          <v-card >
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
              <v-divider class="my-3" ></v-divider>
              <v-icon>mdi-clock</v-icon>Tracked From LinkedIn
            </v-card-text>
          </v-card>
        </v-col>
        <!--  Github  -->
        <v-col cols="3">
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
              <v-divider class="my-3" ></v-divider>
              <v-icon>mdi-clock</v-icon>Tracked From Github
            </v-card-text>
          </v-card>
        </v-col>
        <!--  Twitter  -->
        <v-col cols="3">
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
              <v-divider class="my-3" ></v-divider>
              <v-icon>mdi-clock</v-icon>Tracked From Twitter
            </v-card-text>
          </v-card>
        </v-col>
        <!--  Instagram  -->
        <v-col cols="3">
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
              <v-divider class="my-3" ></v-divider>
              <v-icon>mdi-clock</v-icon>Tracked From Instagram
            </v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-container>

<!--    Latest Development Activities on Github  -->
    <v-container>
      <v-row>
        <v-col cols="12">
          <h2>Latest Github Activities</h2>
        </v-col>
        <v-col cols="8">
          <v-card>
            <v-card-title>
              <v-avatar color="orange" size="62">
                <v-img :src="githubData.avatar_url"></v-img>
              </v-avatar>
              <div class="ml-4 subtitle-1">
                <div class="mb-1">Username: <v-chip color="primary">
                  <v-icon class="mr-1">mdi-account-outline</v-icon>
                  {{githubData.login}}</v-chip>
                </div>
                <div class="mb-1">Location: <v-chip color="info"><v-icon class="mr-1" left>mdi-map-marker</v-icon>{{githubData.location}}</v-chip></div>
                <div class="mb-1">Hireable: <v-chip color="success"><v-icon class="mr-1">{{githubData.hireable? "mdi-account-check" : "mdi-account-off"}}</v-icon>{{githubData.hireable? "Yes" : "No"}}</v-chip></div>
              </div>
            </v-card-title>
            <v-card-text>
              <div v-if="githubEventData.length > 0" v-for=" x in 3">
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
                <v-divider class="mb-3 mt-1"></v-divider>
              </div>
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
        githubEventData: []
      }
    },
    async created() {
      const res = await axios.get("https://api.github.com/users/chclaude")
      .catch(error => console.log(error));

      const resEvent = await axios.get("https://api.github.com/users/ChClaude/events")
        .catch(error => console.log(error));

      if (res !== undefined && resEvent !== undefined) {
        this.githubData = res.data;
        this.githubEventData = resEvent.data;
      }

      console.log("Login");
      console.log(process.env.githubClientId);
      console.log(process.env.githubClientSecret);
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
  .icon-pos {
    position: relative;
    top: -37px;
  }

  .card-tile-height {
    max-height: 70px;
  }

  .card-tile-height a {
    text-decoration: none;
  }

  .height-430 {
    height: 430px;
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

  .android-card {
    display: flex;
    align-items: center;
    flex-flow: column;
  }

  .vue-img {
    position: relative;
    top: 25px;
  }

  .rt-80 {
    position: relative;
    top: -80px;
  }
</style>
