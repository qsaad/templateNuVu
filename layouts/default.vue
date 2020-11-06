<template>
  <v-app dark>
    <!-- <v-navigation-drawer
      v-model="drawer"
      :mini-variant="miniVariant"
      :clipped="clipped"
      dense
      fixed
      app
    >
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
    </v-navigation-drawer> -->
    <v-app-bar
      :clipped-left="clipped"
      dense
      fixed
      app
    >

     <v-avatar size="30" tile >
            <img src="/images/logo.png">
        </v-avatar>
      <v-spacer />
      <!-- <v-app-bar-nav-icon @click.stop="drawer = !drawer" />
      <v-btn
        icon
        @click.stop="miniVariant = !miniVariant"
      >
        <v-icon>mdi-{{ `chevron-${miniVariant ? 'right' : 'left'}` }}</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="clipped = !clipped"
      >
        <v-icon>mdi-application</v-icon>
      </v-btn>
      <v-btn
        icon
        @click.stop="fixed = !fixed"
      >
        <v-icon>mdi-minus</v-icon>
      </v-btn>
      <v-toolbar-title v-text="title" />
      <v-spacer />
      <v-btn
        icon
        @click.stop="rightDrawer = !rightDrawer"
      >
        <v-icon>mdi-menu</v-icon>
      </v-btn> -->

       <v-menu open-on-click left offset-x top >
        <template v-slot:activator="{ on }">
          <v-btn icon v-on="on">
            <v-avatar color="yellow--text title" size=36 v-on="on">
              AC
            </v-avatar>
          </v-btn>
        </template>
        <v-list class="py-0 px-0 my-0 mx-0">
            <v-list-item dense v-for="(item, index) in actions" :key="index + 'mn'" @click="action(item.to)" class="mx-0 my-0 py-0 px-3">
              <v-list-item-action class="py-0 px-0 my-0 mx-0">
                <v-icon>{{ item.icon }}</v-icon>
              </v-list-item-action>
              <v-list-item-content class="py-0 px-0 my-0 ml-2 mr-0">
                <v-list-item-title class="text-left body-2">
                  {{item.title}}
                </v-list-item-title>
              </v-list-item-content>
            </v-list-item>
          </v-list>
        </v-menu>
    </v-app-bar>
    <v-main>
      <v-container>
        <nuxt />
      </v-container>
    </v-main>
    <!-- <v-navigation-drawer
      v-model="rightDrawer"
      :right="right"
      temporary
      fixed
    >
      <v-list>
        <v-list-item @click.native="right = !right">
          <v-list-item-action>
            <v-icon light>
              mdi-repeat
            </v-icon>
          </v-list-item-action>
          <v-list-item-title>Switch drawer (click me)</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-navigation-drawer> -->
    <!-- <v-footer
      :absolute="!fixed"
      app
    >
      <span>&copy; {{ new Date().getFullYear() }}</span>
    </v-footer> -->
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: true,
      drawer: false,
      fixed: false,
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Projext360'
    }
  },
  computed:{
    items(){
        return [
          {icon: 'mdi-view-dashboard', title: 'Dashboard', to: '/dashboard'},
          {icon: 'mdi-cog-outline', title: 'Setting', to: '/setting'},
        ]
      },
      actions(){
        return [
          {icon : 'mdi-cog-outline', title:'Setting',  to:'setting'},
          {icon : 'mdi-logout', title:'Logout', to:'logout'}
        ]
        
      }
  },
  methods:{
    action(value){
        if(value == 'setting'){
          this.$router.replace('/setting').catch(err => console.log(err) )
        }
        if(value == 'logout'){
          //this.$store.dispatch('logout')
          this.$router.replace('/').catch(err => console.log(err) )
        }
      },
  }
}
</script>
