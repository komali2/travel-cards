<script setup>
const allergies = ref([])

</script>
<template>
  <div>
    <input type="checkbox" id="hazelnut" value="hazelnut" v-model="allergies" />
    <label for="hazelnut">Hazelnut</label>
    <input type="checkbox" id="peanut" value="peanut" v-model="allergies" />
    <label for="peanut">peanut</label>
    <input type="checkbox" id="hotdog" value="hotdog" v-model="allergies" />
    <label for="hotdog">hotdog</label>
    <div>
      Allergies: {{allergies}}
    </div>
    <LanguagePicker />
  </div>
</template>
