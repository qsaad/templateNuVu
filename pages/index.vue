<template>
<div>
  
  <top-bar-component path="login" name="Login"></top-bar-component>
  
<!-- +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++ -->
<!-- TAGLINE + LOGIN/REGISTER/RESET DIALOG -->
<!-- +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++ -->
  <v-row justify="center" align="center" class="section-one">
    <v-col cols="12" sm="8" md="6" justify="center" align="center" >
      <img src="/images/logo.png" width="200">
        <p class="display-3 font-weight-bold">PROJEXT360</p>
        <p class="body-2 red--text text--darken-3">A free webapp to stay in sync</p>
           <v-btn color="indigo" to="signup">Sign up</v-btn>
      </v-col>
  </v-row>


  <!-- <v-snackbar vertical v-model="snackbar" :timeout="timeout">
    <v-row dense justify="center" align="center">
      <v-col col="12">
        <p class="green--text text-center body-1">Install this webapp on your iphone :</p>
        <p class="green--text text-center body-1">Tap upload button below and Add to Homescreen</p> 
      </v-col>
    </v-row>
    
    <v-btn color="blue" text @click="snackbar = false">
      Close
    </v-btn>
  </v-snackbar> -->

  <!-- +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++ -->
<!-- FOOTER -->
<!-- +++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++++ -->
    <v-footer color="teal darken-4">
      <v-row dense justify="center" align="center">
      <v-col class="text-center" cols="12">
        {{ new Date().getFullYear() }} — <strong>Projext360</strong>
      </v-col>
      </v-row>
    </v-footer>

  </div>
</template>

<script>
//import {fireAuth} from '~/plugins/firebase.js'
import TopBarComponent from '@/components/TopBarComponent'

// const isIos = () => {
//   const userAgent = window.navigator.userAgent.toLowerCase()
//   return /iphone|ipad|ipod/.test( userAgent );
// }

// Detects if device is in standalone mode
// const isInStandaloneMode = () => ('standalone' in window.navigator) && (window.navigator.standalone);

// const appInstall = () => {
//   if(
//       (('standalone' in window.navigator) && !window.navigator.standalone) //IOS
//       ||
//       (!window.matchMedia('display-mode : standalone').matches) //ANDROID
//     )
//     {
//       alert('Add to Homescreen')
//     }
// }

// const check = () => {
//   if (!('serviceWorker' in navigator)) {
//     throw new Error('No Service Worker support!')
//   }
//   if (!('PushManager' in window)) {
//     throw new Error('No Push API Support!')
//   }
// }

// const registerServiceWorker = async () => {
//   const registration = await navigator.serviceWorker.register('/firebase-messaging-sw.js')
//   return registration
// }

// const main = async () => {
//   try{
//     check();
//     let registration = await registerServiceWorker()
//     if(registration){
//       console.log('SW is registered')
//      }
//   }
//   catch(error){
//     console.log('Service Worker ', error.message)
//   }
// }

// if (process.browser) {
//   main()
// }


export default {
  middleware : [],
  components: {TopBarComponent},
  layout : 'landing',
  data: () => ({
      snackbar : false,
      timeout : 6000
  }),//DATA
  async asyncData({store}){
        return{
         
        }//RETURN
    },//ASYNC DATA
    async fetch({store}){
      
    },
    created(){
      //appInstall()
    },//CREATED
    mounted(){
      // if (isIos() && !isInStandaloneMode()) {
      //     this.snackbar = true
      // }
      //this.isLoggedIn
    },//MOUNTED
    watch: {
     
    },//WATCH
    computed:{
      // async isLoggedIn(){
      //   await fireAuth.onAuthStateChanged(user => {
      //     if (user) {
      //       console.log('Already Logged in')
      //       console.log(user)
      //       this.$store.dispatch('setUser', user)
      //     }
      //     else{
      //       this.$router.replace('/').catch(err => console.log(err) )
      //     }
      //   })
      // }//IS LOGGED IN
    },//COMPUTED
    methods:{
     
    },//METHODS  
}
</script>

<style scoped>
.section-one{
  height : 100vh;
}
</style>

