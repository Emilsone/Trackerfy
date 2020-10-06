<template>
   <nav>
       <v-app-bar   app id="app-bar" >
           <v-app-bar-nav-icon @click.stop="drawer = !drawer" class="white--text"></v-app-bar-nav-icon>
           <v-toolbar-title class="text-uppercase ">
               <span class="font-weight-bold white--text">Trackerfy</span>
           </v-toolbar-title>
           <v-spacer></v-spacer>
           <v-menu offset-y>
      <template v-slot:activator="{ on }">
        <v-btn
          text
          v-on="on"
        >
          <v-icon left>expand_more</v-icon>
            <span class="white--text">Menu</span>
        </v-btn>
      </template>
      <v-list flat  class="white--text">
        <v-list-item v-for="link in links"  :key="link.text" router :to="link.route" active-class="border">
          <v-list-item-title >{{link.text}}</v-list-item-title>
        </v-list-item>
      </v-list>
            </v-menu>
            <v-btn text>
                <span class="white--text">Exit</span>
                <v-icon right class="white--text">exit_to_app</v-icon>
             </v-btn>
       </v-app-bar>
      <v-navigation-drawer  v-model="drawer"  app id="navigation-bar"  >
          <v-layout column align-center>
               <v-flex class="mt-5"> 
                    <v-avatar size="100">
                            <img src="/img1.png" alt="">
                    </v-avatar>
                    <p class="white--text subheading mt-1 text-center">Username</p>
               </v-flex>
               <v-flex class="mt-4 mb-4">
                <Popup />
               </v-flex>
          </v-layout>
          <v-list flat class="white--text">
              <v-list-item v-for="link in links"  :key="link.text" router :to="link.route" active-class="border" >
                  <v-list-item-action>
                     <v-icon  class="white--text" >{{link.icon}}</v-icon>
                  </v-list-item-action>
                  <v-list-item-content >
                      <v-list-item-title  class="white--text" >{{link.text}}</v-list-item-title>
                  </v-list-item-content>
              </v-list-item>
          </v-list>
      </v-navigation-drawer>
   </nav>
</template>
<script>
import Popup from './Popup.vue'
export default {
   data: () => ({
      drawer: true,
      links :[
          {icon: 'dashboard', text:'Dashboard', route: '/'},
          {icon: 'folder', text:'My Project', route: '/projects'},
          {icon: 'person', text:'Team', route: '/team'}
      ]
     
    }),
    components: {
    Popup
  },

   
}
</script>
<style scoped>
.border {
  border-left: 4px solid #0ba518;
}
#navigation-bar{
  background-color: #16172D !important;
  color: white !important;
}
#app-bar{
  background-color: #010216;
}
</style>
