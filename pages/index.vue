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
            lazy-src="/software_dev.jpg"
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
            lazy-src="/silver-and-black-laptop-computer.jpg"
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
