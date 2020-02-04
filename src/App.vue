<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">


        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          src="https://vignette.wikia.nocookie.net/animalrestaurant/images/7/71/Chef_Gumi.png/revision/latest/top-crop/width/200/height/150"
          width="80"
          height="auto"
        />
        <h2>Animal Restaurant VN Wiki </h2>
      </div>

    </v-app-bar>

    <v-content>
      <HelloWorld/>
    </v-content>
  </v-app>
</template>

<script>
import HelloWorld from './components/HelloWorld';

export default {
  name: 'App',

  components: {
    HelloWorld,
  },

  data: () => ({
    //
  }),
};
</script>
