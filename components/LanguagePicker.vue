<script setup lang="ts">
import _ from 'lodash';

enum languages  {
  'en_US'= 'English',
  'zh_TW' = 'Mandarin, Traditional',
}

const values = ref([]);
const { choices, label } = defineProps<{label: string, choices: keyof languages[]}>()

const mappedItems = _.map(_.pick(languages, choices), (val, key) => { return { title: val, value: key };});


</script>
<template>
  <div>
    <v-autocomplete
      v-model="values"
      :items="mappedItems"
      outlined
      dense
      chips
      small-chips
      :label=label
      multiple
    ></v-autocomplete>
  </div>
</template>
