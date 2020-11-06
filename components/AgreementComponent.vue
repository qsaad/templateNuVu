<template>
    <div class="text-center pb-3">
        <v-dialog v-model="dialog" width="500">
            <template v-slot:activator="{ on, attrs }">
                <v-btn color="red" dark v-bind="attrs" v-on="on">
                Terms and Conditions
                </v-btn>
            </template>

            <v-card>
                <v-card-title class="headline orange lighten-2">
                Terms and Conditions
                </v-card-title>

                <v-card-text class="pt-4">
                    <p class="green--text caption">By visiting the <em class="blue--text">https://projext360.firebaseapp.com</em> from here on refered to as <em class="blue--text">{{name}}</em>, viewing, accessing or otherwise using any of the services or information created, collected, compiled or submitted to <em class="blue--text">{{name}}</em>, you agree to be bound by the following Terms and Conditions of Service. If you do not want to be bound by our Terms your only option is not to visit, view or otherwise use the services of <em class="blue--text">{{name}}</em>. You understand, agree and acknowledge that these Terms constitute a legally binding agreement between you and <em class="blue--text">{{name}}</em> and that your use of {{name}} shall indicate your conclusive acceptance of this agreement.</p>

                    <h5 class="yellow--text subtitle-1">Provision of Services</h5>
                    <p class="green--text caption">You agree and acknowledge that <em class="blue--text">{{name}}</em> is entitled to modify, improve or discontinue any of its services at its sole discretion and without notice to you even if it may result in you being prevented from accessing any information contained in it. Furthermore, you agree and acknowledge that <em class="blue--text">{{name}}</em> is entitled to provide services to you through subsidiaries or affiliated entities.</p>

                    <h5 class="yellow--text subtitle-1">Proprietary Rights</h5>
                    <p class="green--text caption">You acknowledge and agree that <em class="blue--text">{{name}}</em> may contain proprietary and confidential information including trademarks, service marks and patents protected by intellectual property laws and international intellectual property treaties. Our content may not be sold, reproduced, or distributed without our written permission. Any third-party trademarks, service marks and logos are the property of their respective owners. Any further rights not specifically granted herein are reserved.</p>

                    <h5 class="yellow--text subtitle-1">Submitted Content</h5>
                    <p class="green--text caption">When you submit content to <em class="blue--text">{{name}}</em> you simultaneously grant <em class="blue--text">{{name}}</em> an irrevocable, worldwide, royalty free license to publish and display your content worldwide. You confirm and warrant that you have the required authority to grant the above license to <em class="blue--text">{{name}}</em>.</p>

                    <h5 class="yellow--text subtitle-1">Termination of Agreement</h5>
                    <p class="green--text caption">The Terms of this agreement will continue to apply in perpetuity until terminated by either party without notice at any time for any reason. Terms that are to continue in perpetuity shall be unaffected by the termination of this agreement.</p>

                    <h5 class="yellow--text subtitle-1">Disclaimer of Warranties</h5>
                    <p class="green--text caption">You understand and agree that your use of <em class="blue--text">{{name}}</em> is entirely at your own risk and that our services are provided "As Is" and "As Available". <em class="blue--text">{{name}}</em> does not make any express or implied warranties, endorsements or representations whatsoever as to the operation of the <em class="blue--text">{{name}}</em>, information, content, materials, or products. This shall include, but not be limited to, implied warranties of merchantability and fitness for a particular purpose and non-infringement, and warranties that access to or use of the service will be uninterrupted or error-free or that defects in the service will be corrected.</p>

                    <h5 class="yellow--text subtitle-1">Limitation of Liability</h5>
                    <p class="green--text caption">You understand and agree that <em class="blue--text">{{name}}</em> and any of its subsidiaries or affiliates shall in no event be liable for any direct, indirect, incidental, consequential, or exemplary damages. This shall include, but not be limited to damages for loss of profits, business interruption, business reputation or goodwill, loss of programs or information or other intangible loss arising out of the use of or the inability to use the service, or information, or any permanent or temporary cessation of such service or access to information, or the deletion or corruption of any content or information, or the failure to store any content or information. The above limitation shall apply whether or not <em class="blue--text">{{name}}</em> has been advised of or should have been aware of the possibility of such damages. In jurisdictions where the exclusion or limitation of liability for consequential or incidental damages is not allowed the liability of <em class="blue--text">{{name}}</em> is limited to the greatest extent permitted by law.</p>

                    <h5 class="yellow--text subtitle-1">External Content</h5>
                    <p class="green--text caption"><em class="blue--text">{{name}}</em> may include hyperlinks to third-party content, advertising or websites. You acknowledge and agree that <em class="blue--text">{{name}}</em> is not responsible for and does not endorse any advertising, products or resource available from such resources or websites.</p>

                    <h5 class="yellow--text subtitle-1">Jurisdiction</h5>
                    <p class="green--text caption">You expressly understand and agree to submit to the personal and exclusive jurisdiction of the courts of the country, state, province or territory determined solely by <em class="blue--text">{{name}}</em> to resolve any legal matter arising from this agreement or related to your use of <em class="blue--text">{{name}}</em>. If the court of law having jurisdiction, rules that any provision of the agreement is invalid, then that provision will be removed from the Terms and the remaining Terms will continue to be valid.</p>

                    <h5 class="yellow--text subtitle-1">Entire Agreement</h5>
                    <p class="green--text caption">You understand and agree that the above Terms constitute the entire general agreement between you and <em class="blue--text">{{name}}</em>. You may be subject to additional Terms and conditions when you use, purchase or access other services, affiliate services or third-party content or material.</p>

                    <h5 class="yellow--text subtitle-1">Changes to the Terms</h5>
                    <p class="green--text caption"><em class="blue--text">{{name}}</em> reserves the right to modify these Terms from time to time at our sole discretion and without any notice. Changes to our Terms become effective on the date they are posted and your continued use of <em class="blue--text">{{name}}</em> after any changes to Terms will signify your agreement to be bound by them.</p>
                </v-card-text>

                <v-divider></v-divider>

                <v-card-actions>
                    <v-spacer></v-spacer>
                    <v-btn color="primary" text @click="dialog = false">
                        I accept
                    </v-btn>
                </v-card-actions>
            </v-card>
        </v-dialog>
    </div>
</template>

<script>
    export default{
        name: 'agreement',
        data(){
            return{
               dialog: false,
               name : "Projext360"
            }
        },
        mounted(){

        }

    }

</script>

<style scoped>

</style>