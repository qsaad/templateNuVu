<template>
    <div>
        <v-row justify="center" class="pa-0 ma-0">
            <v-col cols="12" md="6">
                <v-toolbar dense flat color="teal--darken-2">
                    <v-icon color="yellow">mdi-cog-outline</v-icon>
                    <v-spacer></v-spacer>
                    <v-toolbar-title class="green--text">
                        <v-chip outlined pill class="title font-weight-bold green--text mt-1" color="success">
                            SETTINGS
                        </v-chip>
                    </v-toolbar-title>
                    
                    <v-spacer></v-spacer>
                </v-toolbar>
                <v-card>
                    <v-card-text class="pa-2">
                        <v-row justify="center" align="center">
                            <v-col cols="12">
                                <p>Avatar Color</p>
                                <div class="d-flex flex-column flex-sm-row">
                                    <div class="justify-center align-self-center">
                                        <v-color-picker 
                                            v-model="selectedColor" 
                                            dot-size="30"
                                            hide-inputs
                                        ></v-color-picker>
                                    </div>
                                    <div class="pl-2 ml-2 mt-2 grow d-flex justify-center align-stretch align-self-center">
                                        <v-btn 
                                            color="indigo" 
                                            @click="updateColor"
                                            
                                        >Update Color</v-btn>
                                    </div>
                                    
                                </div>
                            </v-col>
                          
                        </v-row>
                    </v-card-text>
                </v-card>

            </v-col>
        </v-row>

        <bot-nav-component>
        </bot-nav-component>
    </div>
</template>

<script>
import BotNavComponent from '@/components/BotNavComponent.vue'

export default {
    middleware : [],
    components: {BotNavComponent},
    layout : 'default',
    data: () => ({
        //userId: '',
        //selectedModules: [],
        selectedColor: ''
    }),//DATA
    async asyncData({store,params}){
       return{
           //selectedColor: store.getters.color
       }
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
        toggleModule(item){
            //this.$store.dispatch(`toggleModule`, item.name)
        },
        updateColor(){
            //this.$store.dispatch(`updateColor`, this.selectedColor)
        }
    },//METHODS  
}//EXPORT DEFAULT
</script>

   