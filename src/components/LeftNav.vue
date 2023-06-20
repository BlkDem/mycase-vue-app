<template>
  <v-btn color="primary" icon="mdi-open-in-new" class="menu" size="large"
  @click.stop="drawer = !drawer"
  ></v-btn>
  <v-card>
    <v-layout>
      <v-navigation-drawer
        v-model="drawer"
        temporary
        location="right"
      >
        <v-list-item
          prepend-avatar="https://randomuser.me/api/portraits/men/78.jpg"
          title="John Leider"
        ></v-list-item>

        <v-divider></v-divider>

        <v-list density="compact" nav>
          <v-list-item prepend-icon="mdi-view-dashboard" title="Home" value="home"></v-list-item>
          <v-list-item prepend-icon="mdi-forum" title="About" value="about"></v-list-item>
        </v-list>

        <template v-slot:append>
          <div class="pa-2">
            <v-btn block
              color="primary"
              @click.stop="drawer = !drawer"
            >
              Hide
            </v-btn>
          </div>
        </template>

      </v-navigation-drawer>
    </v-layout>
  </v-card>
</template>

<script>
  export default {
    data () {
      return {
        drawer: null,
      }
    },
  }
</script>

<style scoped>

.menu {
  position: absolute;
  bottom: 32px;
  right: 32px;
}

</style>

