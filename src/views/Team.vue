<template>
  <div class="team">
    <h1 class="subheading grey--text">Team</h1>
    
    <v-container class="my-5">
      <v-row>
        <v-col xs="12" sm="6" md="4" lg="3" v-for="(person, i) in team" :key="i">
          <v-card flat class="text-center ma-3">
            <v-responsive class="pt-4">
              <v-avatar size="100" class="grey lighten-2">
                <img :src="person.avatar" :alt="person.name">
              </v-avatar>
            </v-responsive>
            <v-card-text>
              <div class="subheading">{{ person.name }}</div>
              <div class="grey--text">{{ person.role }}</div>
            </v-card-text>
            <v-card-actions>
              <v-btn depressed color="grey--text">
                <v-icon small left>message</v-icon>
                <span>Message</span>
              </v-btn>
            </v-card-actions>
          </v-card>
        </v-col>
      </v-row>
    </v-container>
  
  </div>
</template>

<script>
export default {
  data() {
    return {
      team: [
        { name: 'The Net Ninja', role: 'Web developer', avatar: '/avatarImg.png' },
        { name: 'Ryu', role: 'Graphic designer', avatar: '/avatarImg.png' },
        { name: 'Chun Li', role: 'Web developer', avatar: '/avatarImg.png' },
        { name: 'Gouken', role: 'Social medial', avatar: '/avatarImg.png' },
        { name: 'Yoshi', role: 'Sales guru', avatar: '/avatarImg.png' },
      ]
    }
  }
}
</script>
