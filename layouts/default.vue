<template>
  <v-app light>
    <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      fixed
      app
    >
      <div class="my-2 mr-4" :class="`d-flex justify-center`">
        <v-avatar size="85">
          <v-img
            src="/mypic.jpeg"
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
        </v-avatar>
      </div>
      <v-list>
        <v-list-item
          v-for="(item, i) in items"
          :key="i"
          :to="item.to"
          router
          exact
        >
          <v-list-item-action>
            <v-icon>{{ item.icon }}</v-icon>
          </v-list-item-action>
          <v-list-item-content>
            <v-list-item-title v-text="item.title" />
          </v-list-item-content>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-app-bar
      :clipped-left="clipped"
      fixed
      app
      class="primary white--text"
    >
      <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="white--text" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
        class="white--text"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="clipped = !clipped"
        class="white--text"
      >
        <v-icon class="white--text">mdi-application</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="fixed = !fixed"
        class="white--text"
      >
        <v-icon class="white--text">mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon class="white--text">mdi-menu</v-icon>
      </v-btn>
    </v-app-bar>
    <v-content class="accent">
      <v-container>
        <nuxt />
      </v-container>
    </v-content>
    <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item>
          <v-list-item-action>
            <v-switch v-model="isDark" label=" Dark Theme" @change="theme"></v-switch>
          </v-list-item-action>
        </v-list-item>
      </v-list>
    </v-navigation-drawer>
    <v-footer
      :fixed="fixed"
      app
      class="primary white--text"
    >
      <span>&copy; {{ new Date().getFullYear() }} Claude Chris - Eagle Stack</span>
    </v-footer>
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      isDark: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: "mdi-emoticon-cool-outline",
          title: "About",
          to: '/about'
        },
        {
          icon: "mdi-laptop",
          title: "Creations",
          to: '/creations'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Skills',
          to: '/skills'
        },
        {
          icon: 'mdi-card-account-mail',
          title: 'Contact',
          to: '/contact'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'C. Chris'
    }
  },
  computed: {
    theme() {
      this.$vuetify.theme.dark = this.isDark;
    }
  },
}
</script>
