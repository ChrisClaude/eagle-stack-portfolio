<template>
  <v-container
    class="fill-height"
    fluid
  >
    <v-row
      align="center"
      justify="center"
    >
      <v-col
        cols="12"
        sm="8"
        md="4"
      >
        <v-card class="elevation-12">
          <v-toolbar
            color="primary"
            dark
            flat
          >
            <v-toolbar-title>Contact</v-toolbar-title>
            <v-spacer></v-spacer>
            <v-tooltip bottom>
              <template v-slot:activator="{ on }">
                <v-btn
                  icon
                  large
                  target="_blank"
                  v-on="on"
                >
                  <v-icon>mdi-information-outline</v-icon>
                </v-btn>
              </template>
              <span>I usually respond in less than 24 hours</span>
            </v-tooltip>
          </v-toolbar>
          <v-card-text>
            <v-form
              method="post"
              data-netlify="true"
              data-netlify-honeypot="bot-field"
              @submit="onSubmit"
              id="message-form"
              name="message-form"
            >
              <input type="hidden" name="form-name" value="send-message" />
              <v-text-field
                label="Name"
                name="name"
                prepend-icon="mdi-account"
                type="text"
                v-model="name"
                required
              ></v-text-field>

              <v-text-field
                id="email"
                label="Email"
                name="email"
                prepend-icon="mdi-lock"
                type="email"
                v-model="email"
                required
              ></v-text-field>

              <v-text-field
                label="Message header"
                name="header"
                prepend-icon="mdi-format-title"
                type="text"
                required
                v-model="messageHeader"
              ></v-text-field>

              <v-textarea
                label="Message"
                name="message"
                prepend-icon="mdi-message-reply-text"
                rows="2"
                v-model="message"
                required
              >
              </v-textarea>
            </v-form>
          </v-card-text>
          <v-card-actions>
            <v-spacer></v-spacer>
            <v-btn color="primary" type="submit" form="message-form">Send</v-btn>
          </v-card-actions>

      <!--    Snackbar      -->
          <v-snackbar
            v-model="snackbarData.snackbar"
            :bottom="snackbarData.y === 'bottom'"
            :color="snackbarData.color"
            :left="snackbarData.x === 'left'"
            :multi-line="snackbarData.mode === 'multi-line'"
            :right="snackbarData.x === 'right'"
            :timeout="snackbarData.timeout"
            :top="snackbarData.y === 'top'"
            :vertical="snackbarData.mode === 'vertical'"
          >
            {{ snackbarData.text }}
            <v-btn
              dark
              text
              @click="snackbarData.snackbar = false"
            >
              Close
            </v-btn>
          </v-snackbar>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
  import axios from "axios";

  export default {
    data() {
      return {
        title: "C. Chris | Contact",
        name: "",
        email: "",
        messageHeader: "",
        message: "",
        snackbarData: {
          "snackbar": false,
          "text": "It's not you it's us, an error on our side.",
          "color": "warning",
          "x": null,
          "y": "top",
          "mode": "",
          "timeout": 3500
        }
      }
    },
    methods: {
      encode (data) {
        return Object.keys(data)
          .map(
            key => `${encodeURIComponent(key)}=${encodeURIComponent(data[key])}`
          )
          .join("&");
      },
      onSubmit(e) {
        e.preventDefault();

        if (this.name !== "" && this.email !== "" && this.messageHeader !== "" && this.message !== "") {
          const sentMessage = {
            "author": this.name,
            "email": this.email,
            "title": this.messageHeader,
            "message": this.message
          };

          const axiosConfig = {
            header: { "Content-Type": "application/x-www-form-urlencoded" }
          };

          axios.post("/",this.encode({
              "form-name": "message-form",
              ...sentMessage
            }),
            axiosConfig
          ).then(() => {
            // console.log(sentMessage);
            this.name = "";
            this.email = "";
            this.messageHeader = "";
            this.message = "";
            this.snackbarData.color = "success";
            this.snackbarData.text = "Your message was sent";
            this.snackbarData.snackbar = true;
          }).catch(err => {
            console.error(err);
            this.snackbarData.color = "error";
            this.snackbarData.text = "An error occurred, Please try again";
            this.snackbarData.snackbar = true;
          });

        } else {
          this.snackbarData.color = "error";
          this.snackbarData.text = "An error occurred, Make sure you fill in all fields";
          this.snackbarData.snackbar = true;
        }

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
