<template>
  <v-toolbar
      dense
      fixed
      app
    >
      
      <v-spacer></v-spacer>
           
      <v-badge
      left
      overlap
      bottom
      @click=""
      color="accent"
      
    >
      <template @click="" v-slot:badge>
        5
      </template>
      <v-icon
        medium
        @click=""
      >
        notifications_active
      </v-icon>
    </v-badge>


      <v-btn icon>
        <v-icon>account_circle</v-icon>
      </v-btn>
    </v-toolbar>
</template>
<script>
export default {
  methods: {
    handleClick: function() {
      this.$root.$emit('toggleDrawer');
    }
  }
}
</script>