<template>
    <div>
        <v-footer :fixed="fixed" app>
            <v-row dense justify="center" align="center">
                <v-col cols="12" align="center">
                     <div class="d-inline-flex flex-column justify-center align-center flex-shrink-0 px-2 ">
                        <v-btn icon to="/dashboard" :active-class="selectedButton" class="mb-2">
                            <v-icon>mdi-share-variant</v-icon>
                        </v-btn>
                        <span class="caption">Dashboard</span>
                    </div>
                    <div class="d-inline-flex flex-column justify-center align-center flex-shrink-0 px-2">
                        <v-btn icon to="/notification" :active-class="selectedButton" class="mb-1">
                            <v-badge color="green" :content="notificationsCount" overlap :value="notificationsCount > 0">
                                <v-icon>mdi-bell-outline</v-icon>
                            </v-badge>
                        </v-btn>
                        <span class="caption pt-0 mt-0">Notifications</span>
                    </div>
                    <div class="d-inline-flex flex-column justify-center align-center flex-shrink-0 px-2">
                        <v-btn icon to="/projects" :active-class="selectedButton" class="mb-2">
                            <v-icon>mdi-apps</v-icon>
                        </v-btn>
                        <span class="caption">Projects</span>
                    </div>
                </v-col>
            </v-row>
        </v-footer>
    </div>
</template>

<script>
export default {
    middleware : [],
    components:{},
    props:{
       
    },
    data(){
        return{
           fixed: false,
           count : 0
        }//RETURN
    },//DATA
    async asyncData({store}){
        
    },//ASYN
    fetch(){

    },
    created(){
        
    },//CREATED
    mounted(){
        
    },//MOUNTED
    watch: {
     
    },//WATCH
    computed:{
        selectedButton(){
            return 'orange'
        },
        notificationsCount(){
            return 1
            //let uid = this.$store.getters['uid']
            //return this.$store.getters['notifications/listByUidCount'](uid)
        },
    },//COMPUTED
    methods:{
       
    },//METHODS  
}
</script>

<style scoped>

</style>
