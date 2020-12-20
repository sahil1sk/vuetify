<template>
  <div class="home">
    <h1>Homepage</h1>

    <!-- so this button will hidden on medium to small sized screens -->
    <v-btn class="hidden-md-and-down">click me</v-btn>

    <!-- shown on medium and small scrren -->
    <v-btn class="hidden-md-and-up">click me</v-btn>

    <!-- hidden on small screens only -->
    <v-btn class="hidden-sm-only">click me</v-btn>

    <v-btn class="pink lighten-2 white--text">click me</v-btn>
    <v-btn depressed color="red">click me</v-btn>
    <v-btn color="pink">click me</v-btn>


    <v-btn class="pink white--text">
      <v-icon left>email</v-icon>
      <span>email me</span>
    </v-btn>

    <v-btn small class="pink white--text">
      <v-icon left small>email</v-icon>
      <span>email me</span>
    </v-btn>

    <v-btn large class="pink white--text">
      <v-icon left large>email</v-icon>
      <span>email me</span>
    </v-btn>
    
    <v-btn fab depressed small dark color="purple">
      <v-icon small>favorite</v-icon>
    </v-btn>
    

  </div>
</template>

<script>
export default {

}
</script>
