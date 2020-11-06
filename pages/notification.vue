<template>
    <div>
        <v-container fluid class="pa-0 ma-0">
            <v-row dense justify="center" align="center">
                <v-col cols="12" sm="6" md="8">
                    <v-card hover height="100%" shaped outlined class="pa-0 ma-0">
                            <v-container fluid class="py-0">
                                <v-row justify="center" >
                                    <v-col cols="12" align="start" class="pt-1 d-flex justify-space-between">
                                        <v-chip outlined pill class="title font-weight-bold mt-1" color="success">
                                            NOTIFICATION
                                        </v-chip>
                                    </v-col>
                                    <v-col cols="12">
                                        <v-card>
                                            No data
                                        </v-card>
                                    </v-col>
                                </v-row>
                            </v-container>
                    </v-card>
                </v-col>
        </v-row>
        </v-container>

        <bot-nav-component>
        </bot-nav-component>

    <!-- +++++++++++++++++++++++++++++++++++++++++++++++++++++++++ -->
    <!-- SNACKBAR -->
    <!-- +++++++++++++++++++++++++++++++++++++++++++++++++++++++++ -->  
        <v-snackbar v-model="snackbar" :color="snackbarColor" :timeout="3000" top>
            {{ snackbarText }}
            <v-btn  color="white" text @click="snackbar = false">
                Close
            </v-btn>
        </v-snackbar>
       
    </div>
</template>

<script>
import BotNavComponent from '@/components/BotNavComponent.vue'
//import * as moment from 'moment'

//let sortBy = require('lodash/sortBy')
//let split = require('lodash/split')
//let map = require('lodash/map')

export default {
    middleware : [],
    components: {BotNavComponent},
    layout : 'default',
    data: () => ({
        fixed: false,
        items: [],
        snackbar: false,
        snackbarText: '',
        snackbarColor: '',
    }),//DATA
    async asyncData({store}){
        return{
            //uid : store.getters['uid'],
        }//RETURN
    },//ASYNC DATA
    async fetch({store}){
      
    },
    created(){
      
    
    },//CREATED
    mounted(){
      
    },//MOUNTED
    watch: {
     
    },//WATCH
    computed:{
       
    },//COMPUTED
    methods:{
      
         
    },//METHODS  
}//EXPORT DEFAULT
</script>

   