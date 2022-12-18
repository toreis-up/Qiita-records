<template>
  <v-dialog>
    <template #[`activator`]="{ on: dialogOn, attrs: dialogAttrs }">
      <v-tooltip bottom>
        <template #[`activator`]="{ on: tooltipOn, attrs: tooltipAttrs }">
        <v-btn v-on="{...dialogOn, ...tooltipOn}" v-bind="{dialogAttrs, tooltipAttrs}" @click="showAny({...dialogOn, ...tooltipOn}, {tooltipAttrs, dialogAttrs})">ぼたん</v-btn>
        </template>
        <span>てすと</span>
      </v-tooltip>
    </template>
    <v-card>
      <v-card-title>
        F12でConsoleをみてみよう
      </v-card-title>
    </v-card>
  </v-dialog>
</template>

<script lang="ts">
import Vue from 'vue';

export default Vue.extend({
  methods: {
    showAny(on: any, attrs: any): void {
      console.log('on is ', on);
      console.log('attrs is ', attrs);
    },
    showClick(event: any) {
      console.log(event);
    }
  }
})
</script>