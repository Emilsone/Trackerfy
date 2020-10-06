<template>
  <div class="team">
    <h1 class="subheading grey--text">Interns</h1>
    <v-container >
      <v-layout row wrap>
         
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
              <v-card class="text-center ma-3">
                <v-responsive class="pt-4">
                   <v-avatar size="100" class="red lighten-2">
                     <img :src="person.avatar" alt="" >
                   </v-avatar>
                </v-responsive>
                <v-card-text>
                  <div class="subheading">{{person.name}}</div>
                  <div class="grey--text">{{person.role}}</div>
                </v-card-text>
                <v-card-actions>
                    <v-btn outlined color="orange">
                        <v-icon small left >message</v-icon>
                        <span>Message</span>
                    </v-btn>
                </v-card-actions>
              </v-card>
        </v-flex>

        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
              <v-card class="text-center ma-3">
                <v-responsive class="pt-4">
                   <v-avatar size="100" class="red lighten-2">
                     <img :src="person.avatar" alt="" >
                   </v-avatar>
                </v-responsive>
                <v-card-text>
                  <div class="subheading">{{person.name}}</div>
                  <div class="grey--text">{{person.role}}</div>
                </v-card-text>
                <v-card-actions>
                    <v-btn outlined color="orange">
                        <v-icon small left >message</v-icon>
                        <span>Message</span>
                    </v-btn>
                </v-card-actions>
              </v-card>
        </v-flex>
        <v-flex xs12 sm6 md4 lg3 v-for="person in team" :key="person.name">
              <v-card class="text-center ma-3">
                <v-responsive class="pt-4">
                   <v-avatar size="100" class="red lighten-2">
                     <img :src="person.avatar" alt="" >
                   </v-avatar>
                </v-responsive>
                <v-card-text>
                  <div class="subheading">{{person.name}}</div>
                  <div class="grey--text">{{person.role}}</div>
                </v-card-text>
                <v-card-actions>
                    <v-btn outlined color="orange">
                        <v-icon small left >message</v-icon>
                        <span>Message</span>
                    </v-btn>
                </v-card-actions>
              </v-card>
        </v-flex>
       
      </v-layout>
    </v-container>
  </div>
</template>

<script>
// @ is an alias to /src


export default {
  name: 'interns',
  components: {
   
  },
  data : () => ({
    team: [
      {name: 'Iyad', role: 'web developer', avatar:'/img1.png'},
      {name: 'Reda', role: 'Graphic designer', avatar:'/img2.png'},
      {name: 'Zineb', role: 'web developer', avatar:'/img3.png'},
      {name: 'Hu TechGroup', role: 'Desktop developer', avatar:'/img4.png'},
    ]
  }),
}
</script>
