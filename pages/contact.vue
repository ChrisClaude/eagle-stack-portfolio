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
            <v-form>
              <v-text-field
                label="Name"
                name="name"
                prepend-icon="mdi-account"
                type="text"
                v-model="name"
                required
              ></v-text-field>

              <v-text-field
                id="password"
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
            <v-btn color="primary" @click="sendMessage">Send</v-btn>
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
      sendMessage() {

        if (this.name !== "" && this.email !== "" && this.messageHeader !== "" && this.message !== "") {
          const sentMessage = {
            "author": this.name,
            "email": this.email,
            "title": this.messageHeader,
            "message": this.message
          }
          console.log(sentMessage);
          this.name = "";
          this.email = "";
          this.messageHeader = "";
          this.message = "";
          this.snackbarData.color = "success";
          this.snackbarData.text = "Your message was sent";
        } else {
          this.snackbarData.color = "error";
          this.snackbarData.text = "An error occurred, Make sure you fill in all fields";
        }

        this.snackbarData.snackbar = true;
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
