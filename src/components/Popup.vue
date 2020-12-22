<template>
  <v-dialog max-width="600px" v-model="dialog">
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
            <v-form class="px-3" ref="form">
                <v-text-field label="Title" v-model="title" prepend-icon="folder" :rules="inputRules"></v-text-field>
                <v-textarea label="Information" v-model="content" prepend-icon="edit" :rules="inputRules"></v-textarea>

                <v-menu>
                    <template v-slot:activator="{ on, attrs }">
                        <v-text-field 
                            :value="due"
                            v-bind="attrs"
                            v-on="on" 
                            label="Due date" 
                            prepend-icon="date_range"
                        ></v-text-field>
                    </template>
                    <v-date-picker v-model="due"></v-date-picker>
                </v-menu>

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
            due: null,
            inputRules: [
                v => v.length >= 3 || 'Minimum length is 3 characters'
            ],
            dialog: false,
        }
    },
    methods: {
        submit() {
            if(this.$refs.form.validate()){
                console.log(this.title, this.content)
                this.dialog = false;
            }        
        }
    }
}
</script>
