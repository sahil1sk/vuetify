<template>
  <v-dialog max-width="600px">
    <template v-slot:activator="{ on, attrs }">
        
        <v-btn 
            v-bind="attrs"
            v-on="on" 
            depressed slot="activator" 
            class="success"
        >
          Add new projects
        </v-btn>

    </template>
    <v-card>
        <v-card-title>
            <p class="heading">Add a New Project</p>
        </v-card-title>
        <v-card-text>
            <v-form class="px-3">
                <v-text-field label="Title" v-model="title" prepend-icon="folder"></v-text-field>
                <v-textarea label="Information" v-model="content" prepend-icon="edit"></v-textarea>
                <v-btn @click="submit" depressed class="success mx-0 mt-3">Add project</v-btn>
            </v-form>
        </v-card-text>
    </v-card>
  </v-dialog>
</template>

<script>
export default {
    data() {
        return {
            title: '',
            content: '',
        }
    },
    methods: {
        submit() {
            console.log(this.title, this.content)        
        }
    }
}
</script>
