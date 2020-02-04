<template>
  <v-container>
    <v-layout
      text-center
      wrap
    >
      <Staff></Staff>
    </v-layout>
  </v-container>
</template>

<script>
import Staff from './Staff';

export default {
  name: 'HelloWorld',
  components: {
    Staff,
  },
  data: () => ({
  }),
};
</script>
