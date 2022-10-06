<script setup lang="ts">

const values = ref([]);
const props = defineProps<{label: string}>()

enum languages  {
  'en_US'= 'English',
  'zh_TW' = 'Mandarin, Traditional',
}

const mappedItems = Object.keys(languages).map((key)=>{
  return {
    title: languages[key],
    value: key,
  };
})
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
      label={{label}}
      multiple
    ></v-autocomplete>
  </div>
</template>
