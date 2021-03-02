<template>
  <v-app-bar
      app
      color="primary"
      dark
    >
    <v-container>
        <v-row>
      <div class="d-flex align-left">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer></v-spacer>
      <v-form class="mt-4">
          <v-text-field
            label="Search..."
            single-line            
          ></v-text-field>
      </v-form>
      
      </v-row>
      </v-container>
    </v-app-bar>
</template>

<script>
export default {
    name:"Header",
 
    methods:{
        
    }

}
</script>

<style>

</style>