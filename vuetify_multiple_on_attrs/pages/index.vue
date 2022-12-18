<template>
  <v-container>
  <v-row>
    <v-col>
      <h2>activator check!</h2>
      <Test></Test>
    </v-col>
  </v-row>
</v-container>
</template>

<script lang="ts">
import Vue from 'vue';
import Test from '~/components/Test.vue';

export default Vue.extend({
  name: 'IndexPage',
  components: { Test }
})
</script>
