<template>
  <h2 id="outputField" class="text-success">{{translatedText}}</h2>
</template>

<script>
export default {
  name: 'translateOutput',
  props:['translatedText']
}
</script>

<style>
  #outputField {
    padding-top : 20px;
  }
</style>