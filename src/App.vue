<template>
    <v-app>
    <Navbar />
      <!--nav-->

    <v-content>
      <router-view></router-view>
    </v-content>

     <!--footer-->

  </v-app>
</template>

<script>
import Navbar from '@/views/Navbar'


export default {
  name: 'App',
  components: {Navbar},

  data: () => ({
    //
  }),
};
</script>
