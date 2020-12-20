<template>
  <div class="dashboard">
    <h1 class="subheading grey--text">Dashboard</h1>

    <v-container class="my-5">
    
      <v-layout row wrap>
        <v-flex xs12 md6> <!-- on small screen 12 column on medium tak 6 column-->
          <v-btn outlined block class="primary--text ma-1">1</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary--text ma-1">1</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary--text ma-1">1</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outlined block class="primary--text ma-1">1</v-btn>
        </v-flex>
      </v-layout>

      <v-layout row wrap justify-space-around>
        <v-flex xs4 md3>
          <v-btn outlined block class="success-text ma-1">1</v-btn>
        </v-flex>
        <v-flex xs4 md3>
          <v-btn outlined block class="success-text ma-1">2</v-btn>
        </v-flex>
      </v-layout>
    
    </v-container>

  </div>
</template>

<script>
export default {

}
</script>
